# API Overview

This section assumes you have created an API token and can access the API (see <a data-reference="api_guide:authenticating:api_tokens">API Tokens</a>)

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin efficitur ipsum vitae ligula tristique, vitae dapibus mauris lacinia. Proin rhoncus aliquam nulla at pellentesque. Pellentesque interdum elementum maximus. Aenean tristique, nulla sed convallis blandit, massa elit dignissim ligula, eu aliquam mauris magna at diam. Integer in tellus ac risus suscipit rutrum sed et erat. In in elit porttitor, bibendum nisl eu, tincidunt lectus. Integer ac imperdiet nunc.

## Praesent a Lacinia Purus.

Praesent a lacinia purus. Duis viverra elit est, non consectetur risus imperdiet ut. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis eget ultricies ex. Nam pharetra libero placerat, condimentum lorem vitae, bibendum sapien. Nam quis bibendum lorem. Ut at urna lacus. Quisque in nulla urna.

Integer posuere sem lorem, ac accumsan orci dapibus at. Donec volutpat orci turpis, id lacinia lorem auctor sit amet. Nulla finibus, nisl id mollis pretium, nulla magna eleifend leo, a sagittis neque dui at lectus. Curabitur eleifend, justo sed venenatis sagittis, sem ex iaculis diam, non facilisis tellus ipsum ut nulla. Curabitur erat risus, congue eu ligula vel, eleifend pharetra metus. Suspendisse odio ex, pharetra in feugiat id, luctus sed ante. Duis rutrum diam vel semper tincidunt. Nullam in gravida turpis. Fusce et tincidunt dui. Quisque tincidunt, justo quis vehicula maximus, enim quam laoreet nisl, quis vestibulum ligula mi sit amet sem. Mauris id velit at odio tincidunt semper. Sed non convallis leo.

## Mauris Quis

Mauris quis viverra mauris, non eleifend augue.

- Donec commodo vestibulum risus nec volutpat.
- Vestibulum urna sapien, placerat ut purus vitae, aliquam tincidunt augue.
- Etiam vitae velit sodales, posuere urna ut, sodales magna.
- Nam et iaculis sem.
- Curabitur eu odio vehicula, tempus sem id, mollis purus.
- Aliquam ut risus a libero mattis hendrerit.
- Sed sit amet sollicitudin tellus.

Phasellus maximus, nulla ac suscipit pellentesque, magna nisi sodales mi, sit amet convallis est eros tempus quam. Fusce nec sollicitudin velit. Cras diam nisi, consequat quis tempor in, tristique eget neque. Aliquam ultrices rutrum suscipit. Suspendisse malesuada, massa eget scelerisque lobortis, lectus ligula accumsan nunc, eu tempor massa purus in augue. Morbi at gravida eros. Cras lobortis neque at viverra tincidunt. Nulla finibus gravida elementum. Praesent feugiat pretium metus, ac pellentesque nisi ullamcorper at. Quisque cursus efficitur commodo. Fusce rutrum eros enim, sit amet scelerisque lectus dapibus vel. Donec porttitor eu neque eu ultrices. Suspendisse maximus imperdiet ipsum, at rhoncus lacus dignissim quis. Etiam metus justo, consequat id imperdiet et, sodales a eros.

# General Usage

The table below gives an overview of the possible actions available for an API endpoint.

| Action                                                  | HTTP Method | URI            | Response Code | Description                         | Returns                                                          |
| ------------------------------------------------------- | ----------- | -------------- | ------------- | ----------------------------------- | ---------------------------------------------------------------- |
| **List** resources                                      | GET         | /resources     | 200           | Successful query                    | A representation of a list of resources, optionally filtered     |
|                                                         |             |                | 400           | Client Error, (e.g. invalid params) | No content, or a description of the error if applicable/possible |
|                                                         |             |                | 403           | Unauthorized                        | Explanation of authorization failure                             |
| **Show** detailed information about a specific resource | GET         | /resources/:id | 200           | Successful                          | A representation of the resource with given id                   |
|                                                         |             |                | 403           | Unauthorized                        | Explanation of authorization failure                             |
|                                                         |             |                | 404           | No resource matching id             | No content                                                       |
| **Create** a new resource                               | POST        | /resources     | 200           | Successful creation of resource     | A representation of the new resource                             |
|                                                         |             |                | 400           | Client Error, (e.g. invalid params) | A description of the error(s)                                    |
|                                                         |             |                | 403           | Unauthorized                        | Explanation of authorization failure                             |
| **Update** an existing resource                         | PUT         | /resources/:id | 200           | Successful update of resource       | A representation of the new state of the resource                |
|                                                         |             |                | 400           | Client Error, (e.g. invalid params) | A description of the error(s)                                    |
|                                                         |             |                | 403           | Unauthorized                        | Explanation of authorization failure                             |
|                                                         |             |                | 404           | No resource                         | No content matching id                                           |
| **Delete** an existing resource                         | DELETE      | /resources/:id | 200           | Successful deletion of resource     | A representation of the deleted resource                         |
|                                                         |             |                | 403           | Unauthorized                        | Explanation of authorization failure                             |
|                                                         |             |                | 404           | No resource                         | No content matching id                                           |
