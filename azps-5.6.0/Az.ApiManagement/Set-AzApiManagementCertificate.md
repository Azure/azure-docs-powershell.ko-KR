---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 12FC21EB-0B4E-4275-88FB-7FF42730A6A0
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/set-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementCertificate.md
ms.openlocfilehash: bb60ce1fc2cb20a24d1b445cf4a3729bf26747ce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965440"
---
# <span data-ttu-id="81202-101">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="81202-101">Set-AzApiManagementCertificate</span></span>

## <span data-ttu-id="81202-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81202-102">SYNOPSIS</span></span>
<span data-ttu-id="81202-103">백end과 상호 인증을 위해 구성된 API Management 인증서를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="81202-103">Modifies an API Management certificate which is configured for mutual authentication with backend.</span></span>

## <span data-ttu-id="81202-104">구문</span><span class="sxs-lookup"><span data-stu-id="81202-104">SYNTAX</span></span>

### <span data-ttu-id="81202-105">LoadFromFile(기본값)</span><span class="sxs-lookup"><span data-stu-id="81202-105">LoadFromFile (Default)</span></span>
```
Set-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> -PfxFilePath <String>
 -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81202-106">원시</span><span class="sxs-lookup"><span data-stu-id="81202-106">Raw</span></span>
```
Set-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> -PfxBytes <Byte[]>
 -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81202-107">설명</span><span class="sxs-lookup"><span data-stu-id="81202-107">DESCRIPTION</span></span>
<span data-ttu-id="81202-108">**Set-AzApiManagementCertificate** cmdlet은 Azure API Management 인증서를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="81202-108">The **Set-AzApiManagementCertificate** cmdlet modifies an Azure API Management certificate.</span></span>

## <span data-ttu-id="81202-109">예제</span><span class="sxs-lookup"><span data-stu-id="81202-109">EXAMPLES</span></span>

### <span data-ttu-id="81202-110">예제 1: 인증서 수정</span><span class="sxs-lookup"><span data-stu-id="81202-110">Example 1: Modify a certificate</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -PfxFilePath "C:\contoso\certificates\apimanagementnew.pfx" -PfxPassword "2222"
```

<span data-ttu-id="81202-111">이 명령은 지정된 API Management 인증서를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="81202-111">This command modifies the specified API Management certificate.</span></span>

## <span data-ttu-id="81202-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="81202-112">PARAMETERS</span></span>

### <span data-ttu-id="81202-113">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="81202-113">-CertificateId</span></span>
<span data-ttu-id="81202-114">수정할 인증서의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="81202-114">Specifies the ID of the certificate to modify.</span></span>

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

### <span data-ttu-id="81202-115">-Context</span><span class="sxs-lookup"><span data-stu-id="81202-115">-Context</span></span>
<span data-ttu-id="81202-116">**PsApiManagementContext 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="81202-116">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81202-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81202-117">-DefaultProfile</span></span>
<span data-ttu-id="81202-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="81202-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81202-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="81202-119">-PassThru</span></span>
<span data-ttu-id="81202-120">passthru</span><span class="sxs-lookup"><span data-stu-id="81202-120">passthru</span></span>

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

### <span data-ttu-id="81202-121">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="81202-121">-PfxBytes</span></span>
<span data-ttu-id="81202-122">인증서 파일의 배열을 .pfx 형식으로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="81202-122">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="81202-123">*PfxFilePath* 매개 변수를 지정하지 않으면 이 매개 변수가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="81202-123">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

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

### <span data-ttu-id="81202-124">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="81202-124">-PfxFilePath</span></span>
<span data-ttu-id="81202-125">인증서 파일의 경로를 .pfx 형식으로 지정하여 만들고 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="81202-125">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="81202-126">*PfxBytes* 매개 변수를 지정하지 않으면 이 매개 변수가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="81202-126">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

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

### <span data-ttu-id="81202-127">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="81202-127">-PfxPassword</span></span>
<span data-ttu-id="81202-128">인증서에 대한 암호를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="81202-128">Specifies the password for the certificate.</span></span>

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

### <span data-ttu-id="81202-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81202-129">CommonParameters</span></span>
<span data-ttu-id="81202-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="81202-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81202-131">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="81202-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81202-132">입력</span><span class="sxs-lookup"><span data-stu-id="81202-132">INPUTS</span></span>

### <span data-ttu-id="81202-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="81202-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="81202-134">System.String</span><span class="sxs-lookup"><span data-stu-id="81202-134">System.String</span></span>

### <span data-ttu-id="81202-135">System.Byte[]</span><span class="sxs-lookup"><span data-stu-id="81202-135">System.Byte[]</span></span>

### <span data-ttu-id="81202-136">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="81202-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="81202-137">출력</span><span class="sxs-lookup"><span data-stu-id="81202-137">OUTPUTS</span></span>

### <span data-ttu-id="81202-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="81202-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="81202-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="81202-139">NOTES</span></span>

## <span data-ttu-id="81202-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="81202-140">RELATED LINKS</span></span>

[<span data-ttu-id="81202-141">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="81202-141">Get-AzApiManagementCertificate</span></span>](./Get-AzApiManagementCertificate.md)

[<span data-ttu-id="81202-142">New-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="81202-142">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="81202-143">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="81202-143">Remove-AzApiManagementCertificate</span></span>](./Remove-AzApiManagementCertificate.md)


