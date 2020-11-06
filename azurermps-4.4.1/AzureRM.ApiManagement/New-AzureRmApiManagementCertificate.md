---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5CBEDFF8-C441-44CC-B011-5F5AAFA2E5C6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementCertificate.md
ms.openlocfilehash: 55b95cec3e699872688fad5daeb0d2f7e89059c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531268"
---
# <span data-ttu-id="ab04e-101">New-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="ab04e-101">New-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="ab04e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab04e-102">SYNOPSIS</span></span>
<span data-ttu-id="ab04e-103">백 엔드를 사용 하 여 인증 하는 동안 사용할 API 관리 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ab04e-103">Creates an API Management certificate to be used during Authentication with Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab04e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ab04e-104">SYNTAX</span></span>

### <span data-ttu-id="ab04e-105">파일에서 로드 (기본값)</span><span class="sxs-lookup"><span data-stu-id="ab04e-105">Load from file (Default)</span></span>
```
New-AzureRmApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 -PfxFilePath <String> -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab04e-106">순수</span><span class="sxs-lookup"><span data-stu-id="ab04e-106">Raw</span></span>
```
New-AzureRmApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 -PfxBytes <Byte[]> -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab04e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ab04e-107">DESCRIPTION</span></span>
<span data-ttu-id="ab04e-108">**AzureRmApiManagementCertificate** Cmdlet은 Azure API Management 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ab04e-108">The **New-AzureRmApiManagementCertificate** cmdlet creates an Azure API Management certificate.</span></span>

## <span data-ttu-id="ab04e-109">예제의</span><span class="sxs-lookup"><span data-stu-id="ab04e-109">EXAMPLES</span></span>

### <span data-ttu-id="ab04e-110">예제 1: 인증서 만들기 및 업로드</span><span class="sxs-lookup"><span data-stu-id="ab04e-110">Example 1: Create and upload a certificate</span></span>
```
PS C:\>New-AzureRmApiManagementCertificate -Context $ApiMgmtContext -PfxFilePath "C:\contoso\certificates\apimanagement.pfx" -PfxPassword "1111"
```

<span data-ttu-id="ab04e-111">이 명령은 API Management 인증서를 만들어 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab04e-111">This command creates an API Management certificate and uploads it.</span></span>

## <span data-ttu-id="ab04e-112">변수</span><span class="sxs-lookup"><span data-stu-id="ab04e-112">PARAMETERS</span></span>

### <span data-ttu-id="ab04e-113">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="ab04e-113">-CertificateId</span></span>
<span data-ttu-id="ab04e-114">만들 인증서의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab04e-114">Specifies the ID of the certificate to create.</span></span>
<span data-ttu-id="ab04e-115">이 매개 변수를 지정 하지 않으면 ID가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ab04e-115">If you do not specify this parameter, an ID is generated for you.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab04e-116">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="ab04e-116">-Context</span></span>
<span data-ttu-id="ab04e-117">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab04e-117">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab04e-118">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="ab04e-118">-PfxBytes</span></span>
<span data-ttu-id="ab04e-119">.Pfx 형식의 인증서 파일 바이트 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab04e-119">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="ab04e-120">*PfxFilePath* 매개 변수를 지정 하지 않으면이 매개 변수가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab04e-120">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: Raw
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab04e-121">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="ab04e-121">-PfxFilePath</span></span>
<span data-ttu-id="ab04e-122">.Pfx 형식의 인증서 파일에 대 한 경로를 만들고 업로드할 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab04e-122">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="ab04e-123">*PfxBytes* 매개 변수를 지정 하지 않으면이 매개 변수가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab04e-123">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Load from file
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab04e-124">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="ab04e-124">-PfxPassword</span></span>
<span data-ttu-id="ab04e-125">인증서에 대 한 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab04e-125">Specifies the password for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab04e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab04e-126">-DefaultProfile</span></span>
<span data-ttu-id="ab04e-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ab04e-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab04e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab04e-128">CommonParameters</span></span>
<span data-ttu-id="ab04e-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab04e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab04e-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab04e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab04e-131">입력</span><span class="sxs-lookup"><span data-stu-id="ab04e-131">INPUTS</span></span>

## <span data-ttu-id="ab04e-132">출력</span><span class="sxs-lookup"><span data-stu-id="ab04e-132">OUTPUTS</span></span>

### <span data-ttu-id="ab04e-133">ApiManagement. ServiceManagement. \ PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="ab04e-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="ab04e-134">상속자</span><span class="sxs-lookup"><span data-stu-id="ab04e-134">NOTES</span></span>

## <span data-ttu-id="ab04e-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ab04e-135">RELATED LINKS</span></span>

[<span data-ttu-id="ab04e-136">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="ab04e-136">Get-AzureRmApiManagementCertificate</span></span>](./Get-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="ab04e-137">제거-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="ab04e-137">Remove-AzureRmApiManagementCertificate</span></span>](./Remove-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="ab04e-138">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="ab04e-138">Set-AzureRmApiManagementCertificate</span></span>](./Set-AzureRmApiManagementCertificate.md)


