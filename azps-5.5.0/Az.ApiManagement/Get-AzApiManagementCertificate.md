---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6F7C6611-5C56-4F1D-AB98-CDD92D88821C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCertificate.md
ms.openlocfilehash: 9826de76a65fe097d2daba106bd74df5e94a730e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205800"
---
# <span data-ttu-id="ff259-101">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="ff259-101">Get-AzApiManagementCertificate</span></span>

## <span data-ttu-id="ff259-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff259-102">SYNOPSIS</span></span>
<span data-ttu-id="ff259-103">서비스에서 백end를 통해 상호 인증을 위해 구성된 API Management 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ff259-103">Gets API Management certificates configured for Mutual Authentication with Backend in the service.</span></span>

## <span data-ttu-id="ff259-104">구문</span><span class="sxs-lookup"><span data-stu-id="ff259-104">SYNTAX</span></span>

### <span data-ttu-id="ff259-105">ContextParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="ff259-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff259-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff259-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementCertificate [-CertificateId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff259-107">설명</span><span class="sxs-lookup"><span data-stu-id="ff259-107">DESCRIPTION</span></span>
<span data-ttu-id="ff259-108">**Get-AzApiManagementCertificate** cmdlet은 사용자가 지정한 모든 Azure API Management 인증서 또는 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ff259-108">The **Get-AzApiManagementCertificate** cmdlet gets all Azure API Management certificates or certificates that you specify.</span></span>

## <span data-ttu-id="ff259-109">예제</span><span class="sxs-lookup"><span data-stu-id="ff259-109">EXAMPLES</span></span>

### <span data-ttu-id="ff259-110">예제 1: 모든 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ff259-110">Example 1: Get all certificates</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext
```

<span data-ttu-id="ff259-111">이 명령은 모든 API Management 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ff259-111">This command gets all API Management certificates.</span></span>

### <span data-ttu-id="ff259-112">예제 2: ID로 인증서를 얻게</span><span class="sxs-lookup"><span data-stu-id="ff259-112">Example 2: Get a certificate by its ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789"
```

<span data-ttu-id="ff259-113">이 명령은 지정된 ID로 API Management 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ff259-113">This command gets the API Management certificate with the specified ID.</span></span>

## <span data-ttu-id="ff259-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ff259-114">PARAMETERS</span></span>

### <span data-ttu-id="ff259-115">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="ff259-115">-CertificateId</span></span>
<span data-ttu-id="ff259-116">얻을 인증서의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ff259-116">Specifies the ID of the certificate to get.</span></span>

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

### <span data-ttu-id="ff259-117">-Context</span><span class="sxs-lookup"><span data-stu-id="ff259-117">-Context</span></span>
<span data-ttu-id="ff259-118">**PsApiManagementContext 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="ff259-118">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff259-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff259-119">-DefaultProfile</span></span>
<span data-ttu-id="ff259-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ff259-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff259-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ff259-121">-ResourceId</span></span>
<span data-ttu-id="ff259-122">인증서의 Arm 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="ff259-122">Arm Resource Identifier of the Certificate.</span></span> <span data-ttu-id="ff259-123">지정된 경우 식별자에 의해 인증서를 찾으려고 시도합니다.</span><span class="sxs-lookup"><span data-stu-id="ff259-123">If specified will try to find certificate by the identifier.</span></span> <span data-ttu-id="ff259-124">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="ff259-124">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff259-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ff259-125">-Confirm</span></span>
<span data-ttu-id="ff259-126">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ff259-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff259-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff259-127">-WhatIf</span></span>
<span data-ttu-id="ff259-128">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ff259-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff259-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ff259-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff259-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff259-130">CommonParameters</span></span>
<span data-ttu-id="ff259-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ff259-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff259-132">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ff259-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff259-133">입력</span><span class="sxs-lookup"><span data-stu-id="ff259-133">INPUTS</span></span>

### <span data-ttu-id="ff259-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ff259-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ff259-135">System.String</span><span class="sxs-lookup"><span data-stu-id="ff259-135">System.String</span></span>

## <span data-ttu-id="ff259-136">출력</span><span class="sxs-lookup"><span data-stu-id="ff259-136">OUTPUTS</span></span>

### <span data-ttu-id="ff259-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="ff259-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="ff259-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ff259-138">NOTES</span></span>

## <span data-ttu-id="ff259-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ff259-139">RELATED LINKS</span></span>

[<span data-ttu-id="ff259-140">New-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="ff259-140">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="ff259-141">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="ff259-141">Remove-AzApiManagementCertificate</span></span>](./Remove-AzApiManagementCertificate.md)

[<span data-ttu-id="ff259-142">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="ff259-142">Set-AzApiManagementCertificate</span></span>](./Set-AzApiManagementCertificate.md)


