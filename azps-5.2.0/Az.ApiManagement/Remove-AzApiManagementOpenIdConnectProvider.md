---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 80B61E7D-14DC-422A-8EE3-CAC49EF1BE8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: ab278dcf56646463e1ccbc8ada9baa896b1759bf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361334"
---
# <span data-ttu-id="dbc25-101">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="dbc25-101">Remove-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="dbc25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbc25-102">SYNOPSIS</span></span>
<span data-ttu-id="dbc25-103">OpenID Connect 공급자를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="dbc25-103">Removes an OpenID Connect provider.</span></span>

## <span data-ttu-id="dbc25-104">구문</span><span class="sxs-lookup"><span data-stu-id="dbc25-104">SYNTAX</span></span>

```
Remove-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> -OpenIdConnectProviderId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbc25-105">설명</span><span class="sxs-lookup"><span data-stu-id="dbc25-105">DESCRIPTION</span></span>
<span data-ttu-id="dbc25-106">**Remove-AzApiManagementOpenIdConnectProvider** cmdlet은 Azure API Management용 OpenID Connect 공급자를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="dbc25-106">The **Remove-AzApiManagementOpenIdConnectProvider** cmdlet removes an OpenID Connect provider for Azure API Management.</span></span>

## <span data-ttu-id="dbc25-107">예제</span><span class="sxs-lookup"><span data-stu-id="dbc25-107">EXAMPLES</span></span>

### <span data-ttu-id="dbc25-108">예제 1: 공급자 제거</span><span class="sxs-lookup"><span data-stu-id="dbc25-108">Example 1: Remove a provider</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01" -PassThru
```

<span data-ttu-id="dbc25-109">이 명령은 ID OICProvider01이 있는 공급자를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="dbc25-109">This command removes a provider that has the ID OICProvider01.</span></span>

## <span data-ttu-id="dbc25-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dbc25-110">PARAMETERS</span></span>

### <span data-ttu-id="dbc25-111">-Context</span><span class="sxs-lookup"><span data-stu-id="dbc25-111">-Context</span></span>
<span data-ttu-id="dbc25-112">**PsApiManagementContext 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="dbc25-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="dbc25-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbc25-113">-DefaultProfile</span></span>
<span data-ttu-id="dbc25-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dbc25-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dbc25-115">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="dbc25-115">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="dbc25-116">이 cmdlet이 제거하는 공급자의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dbc25-116">Specifies an ID of the provider that this cmdlet removes.</span></span>

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

### <span data-ttu-id="dbc25-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dbc25-117">-PassThru</span></span>
<span data-ttu-id="dbc25-118">작업이 성공하거나 그렇지 않은 경우 이 cmdlet이 $True 값을 $False 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="dbc25-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="dbc25-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dbc25-119">-Confirm</span></span>
<span data-ttu-id="dbc25-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="dbc25-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbc25-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbc25-121">-WhatIf</span></span>
<span data-ttu-id="dbc25-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="dbc25-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbc25-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dbc25-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbc25-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbc25-124">CommonParameters</span></span>
<span data-ttu-id="dbc25-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="dbc25-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbc25-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="dbc25-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbc25-127">입력</span><span class="sxs-lookup"><span data-stu-id="dbc25-127">INPUTS</span></span>

### <span data-ttu-id="dbc25-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="dbc25-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="dbc25-129">System.String</span><span class="sxs-lookup"><span data-stu-id="dbc25-129">System.String</span></span>

### <span data-ttu-id="dbc25-130">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="dbc25-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="dbc25-131">출력</span><span class="sxs-lookup"><span data-stu-id="dbc25-131">OUTPUTS</span></span>

### <span data-ttu-id="dbc25-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="dbc25-132">System.Boolean</span></span>

## <span data-ttu-id="dbc25-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="dbc25-133">NOTES</span></span>

## <span data-ttu-id="dbc25-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dbc25-134">RELATED LINKS</span></span>

[<span data-ttu-id="dbc25-135">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="dbc25-135">Get-AzApiManagementOpenIdConnectProvider</span></span>](./Get-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="dbc25-136">New-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="dbc25-136">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="dbc25-137">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="dbc25-137">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


