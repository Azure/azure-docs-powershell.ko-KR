---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 80B61E7D-14DC-422A-8EE3-CAC49EF1BE8B
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 3d7d6600e7e26202c920499a615f4124767c830c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988512"
---
# <span data-ttu-id="0763d-101">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="0763d-101">Remove-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="0763d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0763d-102">SYNOPSIS</span></span>
<span data-ttu-id="0763d-103">OpenID Connect 공급자를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0763d-103">Removes an OpenID Connect provider.</span></span>

## <span data-ttu-id="0763d-104">구문</span><span class="sxs-lookup"><span data-stu-id="0763d-104">SYNTAX</span></span>

```
Remove-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> -OpenIdConnectProviderId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0763d-105">설명</span><span class="sxs-lookup"><span data-stu-id="0763d-105">DESCRIPTION</span></span>
<span data-ttu-id="0763d-106">**Remove-AzApiManagementOpenIdConnectProvider** cmdlet은 Azure API Management용 OpenID Connect 공급자를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0763d-106">The **Remove-AzApiManagementOpenIdConnectProvider** cmdlet removes an OpenID Connect provider for Azure API Management.</span></span>

## <span data-ttu-id="0763d-107">예제</span><span class="sxs-lookup"><span data-stu-id="0763d-107">EXAMPLES</span></span>

### <span data-ttu-id="0763d-108">예제 1: 공급자 제거</span><span class="sxs-lookup"><span data-stu-id="0763d-108">Example 1: Remove a provider</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01" -PassThru
```

<span data-ttu-id="0763d-109">이 명령은 ID OICProvider01이 있는 공급자를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0763d-109">This command removes a provider that has the ID OICProvider01.</span></span>

## <span data-ttu-id="0763d-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0763d-110">PARAMETERS</span></span>

### <span data-ttu-id="0763d-111">-Context</span><span class="sxs-lookup"><span data-stu-id="0763d-111">-Context</span></span>
<span data-ttu-id="0763d-112">**PsApiManagementContext 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="0763d-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="0763d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0763d-113">-DefaultProfile</span></span>
<span data-ttu-id="0763d-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0763d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0763d-115">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="0763d-115">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="0763d-116">이 cmdlet이 제거한 공급자의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0763d-116">Specifies an ID of the provider that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0763d-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0763d-117">-PassThru</span></span>
<span data-ttu-id="0763d-118">이 cmdlet은 작업이 성공하거나 그렇지 않은 경우 $True 값을 $False 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0763d-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="0763d-119">-확인</span><span class="sxs-lookup"><span data-stu-id="0763d-119">-Confirm</span></span>
<span data-ttu-id="0763d-120">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0763d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0763d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0763d-121">-WhatIf</span></span>
<span data-ttu-id="0763d-122">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="0763d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0763d-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0763d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0763d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0763d-124">CommonParameters</span></span>
<span data-ttu-id="0763d-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0763d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0763d-126">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0763d-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0763d-127">입력</span><span class="sxs-lookup"><span data-stu-id="0763d-127">INPUTS</span></span>

### <span data-ttu-id="0763d-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0763d-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0763d-129">System.String</span><span class="sxs-lookup"><span data-stu-id="0763d-129">System.String</span></span>

### <span data-ttu-id="0763d-130">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0763d-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0763d-131">출력</span><span class="sxs-lookup"><span data-stu-id="0763d-131">OUTPUTS</span></span>

### <span data-ttu-id="0763d-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0763d-132">System.Boolean</span></span>

## <span data-ttu-id="0763d-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0763d-133">NOTES</span></span>

## <span data-ttu-id="0763d-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0763d-134">RELATED LINKS</span></span>

[<span data-ttu-id="0763d-135">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="0763d-135">Get-AzApiManagementOpenIdConnectProvider</span></span>](./Get-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="0763d-136">New-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="0763d-136">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="0763d-137">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="0763d-137">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


