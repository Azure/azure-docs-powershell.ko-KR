---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 12FC21EB-0B4E-4275-88FB-7FF42730A6A0
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementCertificate.md
ms.openlocfilehash: 3c31da297b47c5d35c7d7b4eea5c55ca87d9521d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381760"
---
# <span data-ttu-id="48148-101">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="48148-101">Set-AzApiManagementCertificate</span></span>

## <span data-ttu-id="48148-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48148-102">SYNOPSIS</span></span>
<span data-ttu-id="48148-103">백렌드와의 상호 인증을 위해 구성된 API Management 인증서를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="48148-103">Modifies an API Management certificate which is configured for mutual authentication with backend.</span></span>

## <span data-ttu-id="48148-104">구문</span><span class="sxs-lookup"><span data-stu-id="48148-104">SYNTAX</span></span>

### <span data-ttu-id="48148-105">LoadFromFile(기본값)</span><span class="sxs-lookup"><span data-stu-id="48148-105">LoadFromFile (Default)</span></span>
```
Set-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> -PfxFilePath <String>
 -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48148-106">원시</span><span class="sxs-lookup"><span data-stu-id="48148-106">Raw</span></span>
```
Set-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> -PfxBytes <Byte[]>
 -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48148-107">설명</span><span class="sxs-lookup"><span data-stu-id="48148-107">DESCRIPTION</span></span>
<span data-ttu-id="48148-108">**Set-AzApiManagementCertificate** cmdlet은 Azure API Management 인증서를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="48148-108">The **Set-AzApiManagementCertificate** cmdlet modifies an Azure API Management certificate.</span></span>

## <span data-ttu-id="48148-109">예제</span><span class="sxs-lookup"><span data-stu-id="48148-109">EXAMPLES</span></span>

### <span data-ttu-id="48148-110">예제 1: 인증서 수정</span><span class="sxs-lookup"><span data-stu-id="48148-110">Example 1: Modify a certificate</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -PfxFilePath "C:\contoso\certificates\apimanagementnew.pfx" -PfxPassword "2222"
```

<span data-ttu-id="48148-111">이 명령은 지정된 API Management 인증서를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="48148-111">This command modifies the specified API Management certificate.</span></span>

## <span data-ttu-id="48148-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="48148-112">PARAMETERS</span></span>

### <span data-ttu-id="48148-113">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="48148-113">-CertificateId</span></span>
<span data-ttu-id="48148-114">수정할 인증서의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="48148-114">Specifies the ID of the certificate to modify.</span></span>

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

### <span data-ttu-id="48148-115">-Context</span><span class="sxs-lookup"><span data-stu-id="48148-115">-Context</span></span>
<span data-ttu-id="48148-116">**PsApiManagementContext 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="48148-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="48148-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48148-117">-DefaultProfile</span></span>
<span data-ttu-id="48148-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="48148-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48148-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="48148-119">-PassThru</span></span>
<span data-ttu-id="48148-120">passthru</span><span class="sxs-lookup"><span data-stu-id="48148-120">passthru</span></span>

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

### <span data-ttu-id="48148-121">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="48148-121">-PfxBytes</span></span>
<span data-ttu-id="48148-122">인증서 파일의 배열을 .pfx 형식으로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="48148-122">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="48148-123">*PfxFilePath* 매개 변수를 지정하지 않으면 이 매개 변수가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="48148-123">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

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

### <span data-ttu-id="48148-124">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="48148-124">-PfxFilePath</span></span>
<span data-ttu-id="48148-125">만들고 업로드할 인증서 파일의 경로를 .pfx 형식으로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="48148-125">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="48148-126">*PfxBytes* 매개 변수를 지정하지 않으면 이 매개 변수가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="48148-126">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

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

### <span data-ttu-id="48148-127">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="48148-127">-PfxPassword</span></span>
<span data-ttu-id="48148-128">인증서에 대한 암호를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="48148-128">Specifies the password for the certificate.</span></span>

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

### <span data-ttu-id="48148-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48148-129">CommonParameters</span></span>
<span data-ttu-id="48148-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="48148-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48148-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="48148-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48148-132">입력</span><span class="sxs-lookup"><span data-stu-id="48148-132">INPUTS</span></span>

### <span data-ttu-id="48148-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="48148-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="48148-134">System.String</span><span class="sxs-lookup"><span data-stu-id="48148-134">System.String</span></span>

### <span data-ttu-id="48148-135">System.Byte[]</span><span class="sxs-lookup"><span data-stu-id="48148-135">System.Byte[]</span></span>

### <span data-ttu-id="48148-136">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="48148-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="48148-137">출력</span><span class="sxs-lookup"><span data-stu-id="48148-137">OUTPUTS</span></span>

### <span data-ttu-id="48148-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="48148-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="48148-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="48148-139">NOTES</span></span>

## <span data-ttu-id="48148-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="48148-140">RELATED LINKS</span></span>

[<span data-ttu-id="48148-141">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="48148-141">Get-AzApiManagementCertificate</span></span>](./Get-AzApiManagementCertificate.md)

[<span data-ttu-id="48148-142">New-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="48148-142">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="48148-143">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="48148-143">Remove-AzApiManagementCertificate</span></span>](./Remove-AzApiManagementCertificate.md)


