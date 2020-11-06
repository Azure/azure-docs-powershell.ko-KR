---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D4C465CE-1B8A-4CFC-BAA8-21CC66B7D6D6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementHostnameConfiguration.md
ms.openlocfilehash: defd5c046427115e44783d6b34ea7b034edc8317
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526404"
---
# <span data-ttu-id="80346-101">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="80346-101">New-AzureRmApiManagementHostnameConfiguration</span></span>

## <span data-ttu-id="80346-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80346-102">SYNOPSIS</span></span>
<span data-ttu-id="80346-103">PsApiManagementHostnameConfiguration의 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="80346-103">Creates an instance of PsApiManagementHostnameConfiguration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80346-104">구문과</span><span class="sxs-lookup"><span data-stu-id="80346-104">SYNTAX</span></span>

```
New-AzureRmApiManagementHostnameConfiguration -CertificateThumbprint <String> -Hostname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80346-105">설명은</span><span class="sxs-lookup"><span data-stu-id="80346-105">DESCRIPTION</span></span>
<span data-ttu-id="80346-106">**AzureRmApiManagementHostnameConfiguration** Cmdlet은 **PsApiManagementHostnameConfiguration** 의 인스턴스를 만드는 도우미 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="80346-106">The **New-AzureRmApiManagementHostnameConfiguration** cmdlet is a helper command that creates an instance of **PsApiManagementHostnameConfiguration**.</span></span>
<span data-ttu-id="80346-107">이 명령은 Set-AzureRmApiManagementHostnames cmdlet과 함께 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="80346-107">This command is used with the Set-AzureRmApiManagementHostnames cmdlet.</span></span>

## <span data-ttu-id="80346-108">예제의</span><span class="sxs-lookup"><span data-stu-id="80346-108">EXAMPLES</span></span>

### <span data-ttu-id="80346-109">예제 1: PsApiManagementHostnameConfiguration의 인스턴스 만들기 및 초기화</span><span class="sxs-lookup"><span data-stu-id="80346-109">Example 1: Create and initialize an instance of PsApiManagementHostnameConfiguration</span></span>
```
PS C:\>New-AzureRmApiManagementHostnameConfiguration -Hostname "portal.contoso.com" -CertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C"
```

<span data-ttu-id="80346-110">이 명령은 **PsApiManagementHostnameConfiguration** 의 인스턴스를 만들고 초기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="80346-110">This command creates and initializes an instance of **PsApiManagementHostnameConfiguration**.</span></span>

## <span data-ttu-id="80346-111">변수</span><span class="sxs-lookup"><span data-stu-id="80346-111">PARAMETERS</span></span>

### <span data-ttu-id="80346-112">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="80346-112">-CertificateThumbprint</span></span>
<span data-ttu-id="80346-113">인증서 지문을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="80346-113">Specifies the certificate thumbprint.</span></span>
<span data-ttu-id="80346-114">Import-AzureRmApiManagementHostnameCertificate cmdlet을 사용 하 여 인증서를 먼저 가져와야 합니다.</span><span class="sxs-lookup"><span data-stu-id="80346-114">The certificate must be first imported with the Import-AzureRmApiManagementHostnameCertificate cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80346-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80346-115">-DefaultProfile</span></span>
<span data-ttu-id="80346-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="80346-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80346-117">-Hostname</span><span class="sxs-lookup"><span data-stu-id="80346-117">-Hostname</span></span>
<span data-ttu-id="80346-118">이 cmdlet이 **PsApiManagementHostnameConfiguration** 인스턴스를 만드는 사용자 지정 호스트 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="80346-118">Specifies the custom host name for which this cmdlet creates the **PsApiManagementHostnameConfiguration** instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80346-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80346-119">CommonParameters</span></span>
<span data-ttu-id="80346-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="80346-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80346-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80346-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80346-122">입력</span><span class="sxs-lookup"><span data-stu-id="80346-122">INPUTS</span></span>

### <span data-ttu-id="80346-123">않아야</span><span class="sxs-lookup"><span data-stu-id="80346-123">None</span></span>

## <span data-ttu-id="80346-124">출력</span><span class="sxs-lookup"><span data-stu-id="80346-124">OUTPUTS</span></span>

### <span data-ttu-id="80346-125">ApiManagement. PsApiManagementHostnameConfiguration/.</span><span class="sxs-lookup"><span data-stu-id="80346-125">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameConfiguration</span></span>

## <span data-ttu-id="80346-126">상속자</span><span class="sxs-lookup"><span data-stu-id="80346-126">NOTES</span></span>

## <span data-ttu-id="80346-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="80346-127">RELATED LINKS</span></span>

[<span data-ttu-id="80346-128">가져오기-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="80346-128">Import-AzureRmApiManagementHostnameCertificate</span></span>](./Import-AzureRmApiManagementHostnameCertificate.md)

[<span data-ttu-id="80346-129">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="80346-129">Set-AzureRmApiManagementHostnames</span></span>](./Set-AzureRmApiManagementHostnames.md)


