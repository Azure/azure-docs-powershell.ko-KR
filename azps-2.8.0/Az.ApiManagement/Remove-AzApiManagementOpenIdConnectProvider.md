---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 80B61E7D-14DC-422A-8EE3-CAC49EF1BE8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: f148f65a6065040a28f936a5dec64f09ff4045eb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697981"
---
# <span data-ttu-id="19aa4-101">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="19aa4-101">Remove-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="19aa4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19aa4-102">SYNOPSIS</span></span>
<span data-ttu-id="19aa4-103">OpenID Connect provider를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="19aa4-103">Removes an OpenID Connect provider.</span></span>

## <span data-ttu-id="19aa4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="19aa4-104">SYNTAX</span></span>

```
Remove-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> -OpenIdConnectProviderId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19aa4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="19aa4-105">DESCRIPTION</span></span>
<span data-ttu-id="19aa4-106">**AzApiManagementOpenIdConnectProvider** Cmdlet은 Azure API Management 용 OpenID Connect 공급자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="19aa4-106">The **Remove-AzApiManagementOpenIdConnectProvider** cmdlet removes an OpenID Connect provider for Azure API Management.</span></span>

## <span data-ttu-id="19aa4-107">예제의</span><span class="sxs-lookup"><span data-stu-id="19aa4-107">EXAMPLES</span></span>

### <span data-ttu-id="19aa4-108">예제 1: 공급자 제거</span><span class="sxs-lookup"><span data-stu-id="19aa4-108">Example 1: Remove a provider</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01" -PassThru
```

<span data-ttu-id="19aa4-109">이 명령은 ID OICProvider01 인 공급자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="19aa4-109">This command removes a provider that has the ID OICProvider01.</span></span>

## <span data-ttu-id="19aa4-110">변수</span><span class="sxs-lookup"><span data-stu-id="19aa4-110">PARAMETERS</span></span>

### <span data-ttu-id="19aa4-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="19aa4-111">-Context</span></span>
<span data-ttu-id="19aa4-112">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19aa4-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="19aa4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19aa4-113">-DefaultProfile</span></span>
<span data-ttu-id="19aa4-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="19aa4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19aa4-115">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="19aa4-115">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="19aa4-116">이 cmdlet이 제거 하는 공급자의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19aa4-116">Specifies an ID of the provider that this cmdlet removes.</span></span>

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

### <span data-ttu-id="19aa4-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="19aa4-117">-PassThru</span></span>
<span data-ttu-id="19aa4-118">이 cmdlet이 작업이 성공한 경우 $True 값을 반환 하거나 다른 방법으로 $False 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="19aa4-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="19aa4-119">-확인</span><span class="sxs-lookup"><span data-stu-id="19aa4-119">-Confirm</span></span>
<span data-ttu-id="19aa4-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="19aa4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19aa4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19aa4-121">-WhatIf</span></span>
<span data-ttu-id="19aa4-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="19aa4-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19aa4-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="19aa4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19aa4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19aa4-124">CommonParameters</span></span>
<span data-ttu-id="19aa4-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="19aa4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19aa4-126">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="19aa4-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19aa4-127">입력</span><span class="sxs-lookup"><span data-stu-id="19aa4-127">INPUTS</span></span>

### <span data-ttu-id="19aa4-128">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="19aa4-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="19aa4-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="19aa4-129">System.String</span></span>

### <span data-ttu-id="19aa4-130">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="19aa4-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="19aa4-131">출력</span><span class="sxs-lookup"><span data-stu-id="19aa4-131">OUTPUTS</span></span>

### <span data-ttu-id="19aa4-132">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="19aa4-132">System.Boolean</span></span>

## <span data-ttu-id="19aa4-133">상속자</span><span class="sxs-lookup"><span data-stu-id="19aa4-133">NOTES</span></span>

## <span data-ttu-id="19aa4-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="19aa4-134">RELATED LINKS</span></span>

[<span data-ttu-id="19aa4-135">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="19aa4-135">Get-AzApiManagementOpenIdConnectProvider</span></span>](./Get-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="19aa4-136">새로운 AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="19aa4-136">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="19aa4-137">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="19aa4-137">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


