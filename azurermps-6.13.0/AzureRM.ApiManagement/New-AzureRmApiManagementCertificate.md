---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5CBEDFF8-C441-44CC-B011-5F5AAFA2E5C6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementCertificate.md
ms.openlocfilehash: f97f6c59bc1888f511d84ed49e6d1d49a5d7f57f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528680"
---
# <span data-ttu-id="5a8d0-101">New-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="5a8d0-101">New-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="5a8d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a8d0-102">SYNOPSIS</span></span>
<span data-ttu-id="5a8d0-103">백 엔드를 사용 하 여 인증 하는 동안 사용할 API 관리 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5a8d0-103">Creates an API Management certificate to be used during Authentication with Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a8d0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5a8d0-104">SYNTAX</span></span>

### <span data-ttu-id="5a8d0-105">LoadFromFile (기본값)</span><span class="sxs-lookup"><span data-stu-id="5a8d0-105">LoadFromFile (Default)</span></span>
```
New-AzureRmApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 -PfxFilePath <String> -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a8d0-106">순수</span><span class="sxs-lookup"><span data-stu-id="5a8d0-106">Raw</span></span>
```
New-AzureRmApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 -PfxBytes <Byte[]> -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a8d0-107">설명은</span><span class="sxs-lookup"><span data-stu-id="5a8d0-107">DESCRIPTION</span></span>
<span data-ttu-id="5a8d0-108">**AzureRmApiManagementCertificate** Cmdlet은 Azure API Management 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5a8d0-108">The **New-AzureRmApiManagementCertificate** cmdlet creates an Azure API Management certificate.</span></span>

## <span data-ttu-id="5a8d0-109">예제의</span><span class="sxs-lookup"><span data-stu-id="5a8d0-109">EXAMPLES</span></span>

### <span data-ttu-id="5a8d0-110">예제 1: 인증서 만들기 및 업로드</span><span class="sxs-lookup"><span data-stu-id="5a8d0-110">Example 1: Create and upload a certificate</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementCertificate -Context $ApiMgmtContext -PfxFilePath "C:\contoso\certificates\apimanagement.pfx" -PfxPassword "1111"
```

<span data-ttu-id="5a8d0-111">이 명령은 Api Management에 인증서를 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a8d0-111">This command uploads a certificate to Api Management.</span></span> <span data-ttu-id="5a8d0-112">이 인증서는 정책을 사용 하 여 백엔드에 상호 인증 하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5a8d0-112">This certificate can be used for mutual authentication with backend using policies.</span></span>

## <span data-ttu-id="5a8d0-113">변수</span><span class="sxs-lookup"><span data-stu-id="5a8d0-113">PARAMETERS</span></span>

### <span data-ttu-id="5a8d0-114">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="5a8d0-114">-CertificateId</span></span>
<span data-ttu-id="5a8d0-115">만들 인증서의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a8d0-115">Specifies the ID of the certificate to create.</span></span>
<span data-ttu-id="5a8d0-116">이 매개 변수를 지정 하지 않으면 ID가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5a8d0-116">If you do not specify this parameter, an ID is generated for you.</span></span>

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

### <span data-ttu-id="5a8d0-117">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="5a8d0-117">-Context</span></span>
<span data-ttu-id="5a8d0-118">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a8d0-118">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="5a8d0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a8d0-119">-DefaultProfile</span></span>
<span data-ttu-id="5a8d0-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5a8d0-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a8d0-121">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="5a8d0-121">-PfxBytes</span></span>
<span data-ttu-id="5a8d0-122">.Pfx 형식의 인증서 파일 바이트 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a8d0-122">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="5a8d0-123">*PfxFilePath* 매개 변수를 지정 하지 않으면이 매개 변수가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a8d0-123">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

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

### <span data-ttu-id="5a8d0-124">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="5a8d0-124">-PfxFilePath</span></span>
<span data-ttu-id="5a8d0-125">.Pfx 형식의 인증서 파일에 대 한 경로를 만들고 업로드할 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a8d0-125">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="5a8d0-126">*PfxBytes* 매개 변수를 지정 하지 않으면이 매개 변수가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a8d0-126">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: LoadFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a8d0-127">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="5a8d0-127">-PfxPassword</span></span>
<span data-ttu-id="5a8d0-128">인증서에 대 한 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a8d0-128">Specifies the password for the certificate.</span></span>

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

### <span data-ttu-id="5a8d0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a8d0-129">CommonParameters</span></span>
<span data-ttu-id="5a8d0-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a8d0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a8d0-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a8d0-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a8d0-132">입력</span><span class="sxs-lookup"><span data-stu-id="5a8d0-132">INPUTS</span></span>

### <span data-ttu-id="5a8d0-133">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5a8d0-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5a8d0-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5a8d0-134">System.String</span></span>

### <span data-ttu-id="5a8d0-135">Byte []</span><span class="sxs-lookup"><span data-stu-id="5a8d0-135">System.Byte[]</span></span>

## <span data-ttu-id="5a8d0-136">출력</span><span class="sxs-lookup"><span data-stu-id="5a8d0-136">OUTPUTS</span></span>

### <span data-ttu-id="5a8d0-137">ApiManagement. ServiceManagement. \ PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="5a8d0-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="5a8d0-138">상속자</span><span class="sxs-lookup"><span data-stu-id="5a8d0-138">NOTES</span></span>

## <span data-ttu-id="5a8d0-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5a8d0-139">RELATED LINKS</span></span>

[<span data-ttu-id="5a8d0-140">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="5a8d0-140">Get-AzureRmApiManagementCertificate</span></span>](./Get-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="5a8d0-141">제거-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="5a8d0-141">Remove-AzureRmApiManagementCertificate</span></span>](./Remove-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="5a8d0-142">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="5a8d0-142">Set-AzureRmApiManagementCertificate</span></span>](./Set-AzureRmApiManagementCertificate.md)


