<template>
  <article v-if="post" class="blog-detail">
    <!-- {{ post }} -->
    <SocialHead
      :title="post.title"
      :description="post.body[0].children[0].text"
      :image="post.imageUrl"
    />
    <div class="container">
      <div class="row">
        <div class="col-lg-9 col-md-9 col-sm-8">
          <div class="row">
            <div class="col-lg-12">
              <div class="post">
                <div class="image">
                  <img
                    :src="post.imageUrl"
                    class="img-responsive"
                    :alt="post.body[0].children[0].text"
                  />
                </div>
                <h1 v-text="post.title"></h1>
                <div class="clearfix">
                  <div class="meta">
                    <ul>
                      <li>
                        <a
                          :href="`https://baoveanninhphiabac.ga${$route.fullPath}/#ung_tuyen`"
                          class="btn btn-default"
                          >Ứng tuyển ngay</a
                        >
                      </li>
                      <li>tìm việc <a href="#">Bảo vệ An Ninh Phía Bắc</a></li>
                      <li>việc làm <a href="#">Bảo vệ Vĩnh Phúc</a></li>
                    </ul>
                  </div>
                  <div class="like-comment-share">
                    <ul>
                      <li class="like">
                        <a href="#" class="like"
                          ><i class="fa fa-heart"></i>292</a
                        >
                      </li>
                      <li>
                        <a href="#"><i class="fa fa-comment"></i> 21</a>
                      </li>
                      <li>
                        <div
                          class="fb-share-button"
                          :data-href="
                            'https://baoveanninhphiabac.ga' +
                            $route.fullPath +
                            '/'
                          "
                          data-layout="button_count"
                          data-size="small"
                        >
                          <a
                            target="_blank"
                            :href="`https://www.facebook.com/sharer/sharer.php?u=https%3A%2F%2Fbaoveanninhphiabac.ga${encodeURI(
                              $route.fullPath + '/'
                            )}&amp;src=sdkpreparse`"
                            class="fb-xfbml-parse-ignore"
                            >Chia sẻ</a
                          >
                        </div>
                      </li>
                    </ul>
                  </div>
                </div>
                <div class="description">
                  <block-content
                    v-for="child in post.body"
                    :key="child._id"
                    :blocks="child"
                  />
                  <div>
                    <p>
                      Bằng cách chia sẻ tin tuyển dụng:
                      <em>{{ post.title }}</em> bạn đã giúp mình lưu lại cơ hội
                      việc làm này và giúp người thân, bạn bè của bạn, chúng tôi
                      được kết nối thêm cơ hội việc làm mới. Chúng tôi rất vui
                      được kết nối đến bạn khi bạn chia sẻ ngay.
                    </p>
                  </div>
                  <div
                    class="fb-like"
                    :data-href="
                      'https://baoveanninhphiabac.ga' + $route.fullPath + '/'
                    "
                    data-width=""
                    data-layout="button"
                    data-action="like"
                    data-size="small"
                    data-share="true"
                  ></div>
                  <br />
                  <div
                    class="fb-save"
                    :data-uri="
                      'https://baoveanninhphiabac.ga' + $route.fullPath + '/'
                    "
                    data-size="large"
                  ></div>
                </div>
              </div>
              <div id="ung_tuyen" class="leave-a-reply">
                <h3>Ứng tuyển: {{ post.title }}</h3>
                <form
                  id="mc4wp-form-1"
                  class="mc4wp-form mc4wp-form-5"
                  method="post"
                  data-id="5"
                  data-name="Ứng tuyển"
                >
                  <div class="row">
                    <div class="col-lg-4 col-md-4 col-sm-4">
                      <div class="form-group">
                        <label>Họ và tên</label>
                        <input
                          class="form-control"
                          type="text"
                          name="FNAME"
                          required="*"
                        />
                      </div>
                    </div>
                    <div class="col-lg-4 col-md-4 col-sm-4">
                      <div class="form-group">
                        <label>Tuổi</label>
                        <input
                          class="form-control"
                          type="number"
                          name="YEAROLD"
                          required="*"
                        />
                      </div>
                    </div>
                    <div class="col-lg-4 col-md-4 col-sm-4">
                      <div class="form-group">
                        <label>Chiều cao + cân nặng</label>
                        <input
                          class="form-control"
                          type="text"
                          name="BMI"
                          required="*"
                        />
                      </div>
                    </div>
                    <div class="col-lg-4 col-md-4 col-sm-4">
                      <div class="form-group">
                        <label>Địa chỉ hiện tại</label>
                        <input
                          class="form-control"
                          type="text"
                          name="CURRENTADD"
                          required="*"
                        />
                      </div>
                    </div>
                    <div class="col-lg-4 col-md-4 col-sm-4">
                      <div class="form-group">
                        <label>Số điện thoại</label>
                        <input
                          class="form-control"
                          type="tel"
                          name="PHONE"
                          required=""
                        />
                      </div>
                    </div>
                    <div class="col-lg-4 col-md-4 col-sm-4">
                      <div class="form-group">
                        <label>Email nhận thông báo tuyển dụng: </label>
                        <input
                          class="form-control"
                          type="email"
                          name="EMAIL"
                          required="*"
                        />
                        <p>
                          Chúng tôi sẽ gửi email thông báo tuyển dụng đến bạn.
                          (nếu không có email bạn có thể dùng email của bạn bè
                          hoặc người thân để nhận thông báo).
                        </p>
                      </div>
                    </div>

                    <div class="col-lg-12">
                      <div class="button">
                        <input
                          class="btn btn-default"
                          type="submit"
                          value="Có, tôi muốn xin làm bảo vệ"
                        />
                      </div>
                      <p>
                        <br />
                        Hỗ trợ gọi zalo chị Thắm
                        <a href="tel:0978333963">0978 333 963</a> hoặc
                        <a href="https://zalo.me/0978333963">Zalo</a>
                      </p>
                    </div>
                  </div>

                  <label style="display: none !important"
                    >Leave this field empty if you're human:
                    <input
                      type="text"
                      name="_mc4wp_honeypot"
                      value=""
                      tabindex="-1"
                      autocomplete="off" /></label
                  ><input
                    type="hidden"
                    name="_mc4wp_timestamp"
                    value="1621035386"
                  /><input
                    type="hidden"
                    name="_mc4wp_form_id"
                    value="5"
                  /><input
                    type="hidden"
                    name="_mc4wp_form_element_id"
                    value="mc4wp-form-1"
                  />
                  <div class="mc4wp-response"></div>
                </form>
              </div>
            </div>
          </div>
          <script
            async
            defer
            crossorigin="anonymous"
            src="https://connect.facebook.net/vi_VN/sdk.js#xfbml=1&version=v10.0&appId=242726457596775&autoLogAppEvents=1"
            nonce="D6wC9xAj"
          ></script>
          <!-- Your Chat Plugin code -->
          <div
            class="fb-customerchat"
            attribution="setup_tool"
            page_id="110994124405341"
          ></div>
          <div
            class="fb-comments"
            :data-href="'https://baoveanninhphiabac.ga' + $route.fullPath + '/'"
            data-width=""
            data-numposts="5"
          ></div>
        </div>
        <div class="col-lg-3 col-md-3 col-sm-4 sidebar"></div>
      </div>
    </div>
  </article>
</template>

<script>
import { groq } from '@nuxtjs/sanity'
export default {
  async asyncData({ params, $sanity }) {
    const query = groq`*[_type == "post" && slug.current == "${params.slug}"][0]{_id, title, body, slug, 'imageId': mainImage.asset->_id, "imageUrl": mainImage.asset->url}`
    const post = await $sanity.fetch(query)
    return { post }
  },
  head() {
    return {
      title: this.post.title,
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: this.post.body[0].children[0].text,
        },
      ],
      __dangerouslyDisableSanitizers: ['script'],
      script: [
        {
          type: 'application/ld+json',
          json: {
            '@context': 'https://schema.org/',
            '@type': 'JobPosting',
            title: this.post.body[1].children[0].text,
            description:
              '<p>' +
              this.post.body
                .map((block) =>
                  block.children.map((child) => child.text).join('<br> ')
                )
                .join('<br> ') +
              '</p>',
            identifier: {
              '@type': 'PropertyValue',
              name: 'Hồ Thị Thắm',
              value: '84978333963',
            },
            datePosted: new Date().toISOString(),
            validThrough: new Date(
              Date.now() + 29 * 24 * 60 * 60 * 1000
            ).toISOString(),
            employmentType: 'CONTRACTOR',
            hiringOrganization: {
              '@type': 'Organization',
              name: 'Công Ty TNHH Dịch Vụ Bảo Vệ An Ninh Phía Bắc',
              sameAs: 'https://baoveanninhphiabac.ga',
              logo: 'https://baoveanninhphiabac.ga/images/logo.png',
            },
            jobLocation: {
              '@type': 'Place',
              address: {
                '@type': 'PostalAddress',
                streetAddress:
                  '38, Tổ 13, Phường Trưng Trắc, Thị Xã Phúc Yên, Phường Trưng Trắc, Phúc Yên, Vĩnh Phúc',
                addressLocality: 'Vĩnh Phúc',
                addressRegion: 'Vĩnh Phúc',
                postalCode: '15000',
                addressCountry: 'VN',
              },
            },
            baseSalary: {
              '@type': 'MonetaryAmount',
              currency: 'VND',
              value: {
                '@type': 'QuantitativeValue',
                minValue: 14000,
                maxValue: 16000,
                unitText: 'HOUR',
              },
            },
          },
        },
      ],
    }
  },
}
</script>
