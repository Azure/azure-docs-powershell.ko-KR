---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 12FC21EB-0B4E-4275-88FB-7FF42730A6A0
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementCertificate.md
ms.openlocfilehash: b565c616ff493b2721486bc6916238e997397ce6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869350"
---
# <span data-ttu-id="e1a7d-101">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="e1a7d-101">Set-AzApiManagementCertificate</span></span>

## <span data-ttu-id="e1a7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1a7d-102">SYNOPSIS</span></span>
<span data-ttu-id="e1a7d-103">백엔드를 사용 하 여 상호 인증 하도록 구성 된 API Management 인증서를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1a7d-103">Modifies an API Management certificate which is configured for mutual authentication with backend.</span></span>

## <span data-ttu-id="e1a7d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e1a7d-104">SYNTAX</span></span>

### <span data-ttu-id="e1a7d-105">LoadFromFile (기본값)</span><span class="sxs-lookup"><span data-stu-id="e1a7d-105">LoadFromFile (Default)</span></span>
```
Set-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> -PfxFilePath <String>
 -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1a7d-106">순수</span><span class="sxs-lookup"><span data-stu-id="e1a7d-106">Raw</span></span>
```
Set-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> -PfxBytes <Byte[]>
 -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1a7d-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e1a7d-107">DESCRIPTION</span></span>
<span data-ttu-id="e1a7d-108">**AzApiManagementCertificate** Cmdlet은 Azure API Management 인증서를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1a7d-108">The **Set-AzApiManagementCertificate** cmdlet modifies an Azure API Management certificate.</span></span>

## <span data-ttu-id="e1a7d-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e1a7d-109">EXAMPLES</span></span>

### <span data-ttu-id="e1a7d-110">예제 1: 인증서 수정</span><span class="sxs-lookup"><span data-stu-id="e1a7d-110">Example 1: Modify a certificate</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -PfxFilePath "C:\contoso\certificates\apimanagementnew.pfx" -PfxPassword "2222"
```

<span data-ttu-id="e1a7d-111">이 명령은 지정 된 API Management 인증서를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1a7d-111">This command modifies the specified API Management certificate.</span></span>

## <span data-ttu-id="e1a7d-112">변수</span><span class="sxs-lookup"><span data-stu-id="e1a7d-112">PARAMETERS</span></span>

### <span data-ttu-id="e1a7d-113">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="e1a7d-113">-CertificateId</span></span>
<span data-ttu-id="e1a7d-114">수정할 인증서의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1a7d-114">Specifies the ID of the certificate to modify.</span></span>

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

### <span data-ttu-id="e1a7d-115">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="e1a7d-115">-Context</span></span>
<span data-ttu-id="e1a7d-116">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1a7d-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="e1a7d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1a7d-117">-DefaultProfile</span></span>
<span data-ttu-id="e1a7d-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e1a7d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1a7d-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e1a7d-119">-PassThru</span></span>
<span data-ttu-id="e1a7d-120">passthru</span><span class="sxs-lookup"><span data-stu-id="e1a7d-120">passthru</span></span>

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

### <span data-ttu-id="e1a7d-121">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="e1a7d-121">-PfxBytes</span></span>
<span data-ttu-id="e1a7d-122">.Pfx 형식의 인증서 파일 바이트 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1a7d-122">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="e1a7d-123">*PfxFilePath* 매개 변수를 지정 하지 않으면이 매개 변수가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1a7d-123">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

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

### <span data-ttu-id="e1a7d-124">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="e1a7d-124">-PfxFilePath</span></span>
<span data-ttu-id="e1a7d-125">.Pfx 형식의 인증서 파일에 대 한 경로를 만들고 업로드할 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1a7d-125">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="e1a7d-126">*PfxBytes* 매개 변수를 지정 하지 않으면이 매개 변수가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1a7d-126">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

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

### <span data-ttu-id="e1a7d-127">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="e1a7d-127">-PfxPassword</span></span>
<span data-ttu-id="e1a7d-128">인증서에 대 한 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1a7d-128">Specifies the password for the certificate.</span></span>

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

### <span data-ttu-id="e1a7d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1a7d-129">CommonParameters</span></span>
<span data-ttu-id="e1a7d-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1a7d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1a7d-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1a7d-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1a7d-132">입력</span><span class="sxs-lookup"><span data-stu-id="e1a7d-132">INPUTS</span></span>

### <span data-ttu-id="e1a7d-133">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e1a7d-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e1a7d-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e1a7d-134">System.String</span></span>

### <span data-ttu-id="e1a7d-135">Byte []</span><span class="sxs-lookup"><span data-stu-id="e1a7d-135">System.Byte[]</span></span>

### <span data-ttu-id="e1a7d-136">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="e1a7d-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e1a7d-137">출력</span><span class="sxs-lookup"><span data-stu-id="e1a7d-137">OUTPUTS</span></span>

### <span data-ttu-id="e1a7d-138">ApiManagement. ServiceManagement. \ PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="e1a7d-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="e1a7d-139">상속자</span><span class="sxs-lookup"><span data-stu-id="e1a7d-139">NOTES</span></span>

## <span data-ttu-id="e1a7d-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e1a7d-140">RELATED LINKS</span></span>

[<span data-ttu-id="e1a7d-141">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="e1a7d-141">Get-AzApiManagementCertificate</span></span>](./Get-AzApiManagementCertificate.md)

[<span data-ttu-id="e1a7d-142">새로운 AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="e1a7d-142">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="e1a7d-143">제거-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="e1a7d-143">Remove-AzApiManagementCertificate</span></span>](./Remove-AzApiManagementCertificate.md)


