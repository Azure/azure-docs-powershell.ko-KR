---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6F7C6611-5C56-4F1D-AB98-CDD92D88821C
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCertificate.md
ms.openlocfilehash: 1885f8b4f3c72ace4bad55b355e1d16013228611
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972267"
---
# <span data-ttu-id="f1fff-101">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="f1fff-101">Get-AzApiManagementCertificate</span></span>

## <span data-ttu-id="f1fff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1fff-102">SYNOPSIS</span></span>
<span data-ttu-id="f1fff-103">서비스에서 Backend를 통해 상호 인증을 위해 구성된 API Management 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f1fff-103">Gets API Management certificates configured for Mutual Authentication with Backend in the service.</span></span>

## <span data-ttu-id="f1fff-104">구문</span><span class="sxs-lookup"><span data-stu-id="f1fff-104">SYNTAX</span></span>

### <span data-ttu-id="f1fff-105">ContextParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="f1fff-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1fff-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1fff-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementCertificate [-CertificateId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1fff-107">설명</span><span class="sxs-lookup"><span data-stu-id="f1fff-107">DESCRIPTION</span></span>
<span data-ttu-id="f1fff-108">**Get-AzApiManagementCertificate** cmdlet은 지정한 모든 Azure API Management 인증서 또는 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f1fff-108">The **Get-AzApiManagementCertificate** cmdlet gets all Azure API Management certificates or certificates that you specify.</span></span>

## <span data-ttu-id="f1fff-109">예제</span><span class="sxs-lookup"><span data-stu-id="f1fff-109">EXAMPLES</span></span>

### <span data-ttu-id="f1fff-110">예제 1: 모든 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f1fff-110">Example 1: Get all certificates</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext
```

<span data-ttu-id="f1fff-111">이 명령은 모든 API Management 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f1fff-111">This command gets all API Management certificates.</span></span>

### <span data-ttu-id="f1fff-112">예제 2: ID를 통해 인증서를 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f1fff-112">Example 2: Get a certificate by its ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789"
```

<span data-ttu-id="f1fff-113">이 명령은 지정된 ID가 있는 API Management 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f1fff-113">This command gets the API Management certificate with the specified ID.</span></span>

## <span data-ttu-id="f1fff-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f1fff-114">PARAMETERS</span></span>

### <span data-ttu-id="f1fff-115">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="f1fff-115">-CertificateId</span></span>
<span data-ttu-id="f1fff-116">얻을 인증서의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f1fff-116">Specifies the ID of the certificate to get.</span></span>

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

### <span data-ttu-id="f1fff-117">-Context</span><span class="sxs-lookup"><span data-stu-id="f1fff-117">-Context</span></span>
<span data-ttu-id="f1fff-118">**PsApiManagementContext 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="f1fff-118">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="f1fff-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1fff-119">-DefaultProfile</span></span>
<span data-ttu-id="f1fff-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f1fff-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1fff-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1fff-121">-ResourceId</span></span>
<span data-ttu-id="f1fff-122">인증서의 Arm 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="f1fff-122">Arm Resource Identifier of the Certificate.</span></span> <span data-ttu-id="f1fff-123">지정한 경우 식별자에 의해 인증서를 찾으려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1fff-123">If specified will try to find certificate by the identifier.</span></span> <span data-ttu-id="f1fff-124">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="f1fff-124">This parameter is required.</span></span>

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

### <span data-ttu-id="f1fff-125">-확인</span><span class="sxs-lookup"><span data-stu-id="f1fff-125">-Confirm</span></span>
<span data-ttu-id="f1fff-126">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f1fff-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1fff-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1fff-127">-WhatIf</span></span>
<span data-ttu-id="f1fff-128">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="f1fff-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1fff-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f1fff-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1fff-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1fff-130">CommonParameters</span></span>
<span data-ttu-id="f1fff-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f1fff-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1fff-132">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f1fff-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1fff-133">입력</span><span class="sxs-lookup"><span data-stu-id="f1fff-133">INPUTS</span></span>

### <span data-ttu-id="f1fff-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f1fff-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f1fff-135">System.String</span><span class="sxs-lookup"><span data-stu-id="f1fff-135">System.String</span></span>

## <span data-ttu-id="f1fff-136">출력</span><span class="sxs-lookup"><span data-stu-id="f1fff-136">OUTPUTS</span></span>

### <span data-ttu-id="f1fff-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="f1fff-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="f1fff-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f1fff-138">NOTES</span></span>

## <span data-ttu-id="f1fff-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f1fff-139">RELATED LINKS</span></span>

[<span data-ttu-id="f1fff-140">New-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="f1fff-140">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="f1fff-141">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="f1fff-141">Remove-AzApiManagementCertificate</span></span>](./Remove-AzApiManagementCertificate.md)

[<span data-ttu-id="f1fff-142">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="f1fff-142">Set-AzApiManagementCertificate</span></span>](./Set-AzApiManagementCertificate.md)


