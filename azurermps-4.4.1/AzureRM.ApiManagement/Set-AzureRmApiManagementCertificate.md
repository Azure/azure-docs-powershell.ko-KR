---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 12FC21EB-0B4E-4275-88FB-7FF42730A6A0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementCertificate.md
ms.openlocfilehash: ca9305b2d5863276c5d898e310dfab8be7488382
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93710996"
---
# <span data-ttu-id="b2dec-101">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="b2dec-101">Set-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="b2dec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2dec-102">SYNOPSIS</span></span>
<span data-ttu-id="b2dec-103">API Management 인증서를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2dec-103">Modifies an API Management certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2dec-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b2dec-104">SYNTAX</span></span>

### <span data-ttu-id="b2dec-105">파일에서 로드 (기본값)</span><span class="sxs-lookup"><span data-stu-id="b2dec-105">Load from file (Default)</span></span>
```
Set-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 -PfxFilePath <String> -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b2dec-106">순수</span><span class="sxs-lookup"><span data-stu-id="b2dec-106">Raw</span></span>
```
Set-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 -PfxBytes <Byte[]> -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b2dec-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b2dec-107">DESCRIPTION</span></span>
<span data-ttu-id="b2dec-108">**AzureRmApiManagementCertificate** Cmdlet은 Azure API Management 인증서를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2dec-108">The **Set-AzureRmApiManagementCertificate** cmdlet modifies an Azure API Management certificate.</span></span>

## <span data-ttu-id="b2dec-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b2dec-109">EXAMPLES</span></span>

### <span data-ttu-id="b2dec-110">예제 1: 인증서 수정</span><span class="sxs-lookup"><span data-stu-id="b2dec-110">Example 1: Modify a certificate</span></span>
```
PS C:\>Set-AzureRmApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -PfxFilePath "C:\contoso\certificates\apimanagementnew.pfx" -PfxPassword "2222"
```

<span data-ttu-id="b2dec-111">이 명령은 지정 된 API Management 인증서를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2dec-111">This command modifies the specified API Management certificate.</span></span>

## <span data-ttu-id="b2dec-112">변수</span><span class="sxs-lookup"><span data-stu-id="b2dec-112">PARAMETERS</span></span>

### <span data-ttu-id="b2dec-113">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="b2dec-113">-CertificateId</span></span>
<span data-ttu-id="b2dec-114">수정할 인증서의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2dec-114">Specifies the ID of the certificate to modify.</span></span>

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

### <span data-ttu-id="b2dec-115">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="b2dec-115">-Context</span></span>
<span data-ttu-id="b2dec-116">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2dec-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="b2dec-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b2dec-117">-PassThru</span></span>
<span data-ttu-id="b2dec-118">passthru</span><span class="sxs-lookup"><span data-stu-id="b2dec-118">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2dec-119">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="b2dec-119">-PfxBytes</span></span>
<span data-ttu-id="b2dec-120">.Pfx 형식의 인증서 파일 바이트 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2dec-120">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="b2dec-121">*PfxFilePath* 매개 변수를 지정 하지 않으면이 매개 변수가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2dec-121">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

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

### <span data-ttu-id="b2dec-122">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="b2dec-122">-PfxFilePath</span></span>
<span data-ttu-id="b2dec-123">.Pfx 형식의 인증서 파일에 대 한 경로를 만들고 업로드할 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2dec-123">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="b2dec-124">*PfxBytes* 매개 변수를 지정 하지 않으면이 매개 변수가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2dec-124">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

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

### <span data-ttu-id="b2dec-125">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="b2dec-125">-PfxPassword</span></span>
<span data-ttu-id="b2dec-126">인증서에 대 한 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2dec-126">Specifies the password for the certificate.</span></span>

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

### <span data-ttu-id="b2dec-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2dec-127">-DefaultProfile</span></span>
<span data-ttu-id="b2dec-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b2dec-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2dec-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2dec-129">CommonParameters</span></span>
<span data-ttu-id="b2dec-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2dec-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2dec-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2dec-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2dec-132">입력</span><span class="sxs-lookup"><span data-stu-id="b2dec-132">INPUTS</span></span>

## <span data-ttu-id="b2dec-133">출력</span><span class="sxs-lookup"><span data-stu-id="b2dec-133">OUTPUTS</span></span>

### <span data-ttu-id="b2dec-134">ApiManagement. ServiceManagement. \ PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="b2dec-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="b2dec-135">상속자</span><span class="sxs-lookup"><span data-stu-id="b2dec-135">NOTES</span></span>

## <span data-ttu-id="b2dec-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b2dec-136">RELATED LINKS</span></span>

[<span data-ttu-id="b2dec-137">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="b2dec-137">Get-AzureRmApiManagementCertificate</span></span>](./Get-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="b2dec-138">새로운 AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="b2dec-138">New-AzureRmApiManagementCertificate</span></span>](./New-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="b2dec-139">제거-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="b2dec-139">Remove-AzureRmApiManagementCertificate</span></span>](./Remove-AzureRmApiManagementCertificate.md)


