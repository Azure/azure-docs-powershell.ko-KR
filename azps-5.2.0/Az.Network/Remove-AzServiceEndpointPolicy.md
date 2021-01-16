---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicy.md
ms.openlocfilehash: 207a07186cd7284059e0824da1f86afbc22873f5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355221"
---
# <span data-ttu-id="59070-101">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="59070-101">Remove-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="59070-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59070-102">SYNOPSIS</span></span>
<span data-ttu-id="59070-103">서비스 엔드포인트 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="59070-103">Removes a service endpoint policy.</span></span>

## <span data-ttu-id="59070-104">구문</span><span class="sxs-lookup"><span data-stu-id="59070-104">SYNTAX</span></span>

### <span data-ttu-id="59070-105">RemoveByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="59070-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzServiceEndpointPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59070-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="59070-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzServiceEndpointPolicy -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59070-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="59070-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzServiceEndpointPolicy -InputObject <PSServiceEndpointPolicy> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59070-108">설명</span><span class="sxs-lookup"><span data-stu-id="59070-108">DESCRIPTION</span></span>
<span data-ttu-id="59070-109">**Remove-AzServiceEndpointPolicy** cmdlet은 서비스 엔드포인트 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="59070-109">The **Remove-AzServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="59070-110">예제</span><span class="sxs-lookup"><span data-stu-id="59070-110">EXAMPLES</span></span>

### <span data-ttu-id="59070-111">예제 1: 이름을 사용하여 서비스 엔드포인트 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="59070-111">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzServiceEndpointPolicy -Name "Policy1" -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="59070-112">이 명령은 이름이 "resourcegroup1"인 리소스 그룹에 속하는 Policy1 이름의 서비스 엔드포인트 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="59070-112">This command removes a service endpoint policy with name Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

### <span data-ttu-id="59070-113">예제 2: 입력 개체를 사용하여 서비스 엔드포인트 정책 제거</span><span class="sxs-lookup"><span data-stu-id="59070-113">Example 2: Remove a service endpoint policy using input object</span></span>
```
Remove-AzServiceEndpointPolicy -InputObject $Policy1 -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="59070-114">이 명령은 이름이 "resourcegroup1"인 리소스 그룹에 속하는 서비스 엔드포인트 정책 개체 Policy1을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="59070-114">This command removes a service endpoint policy object Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

## <span data-ttu-id="59070-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59070-115">PARAMETERS</span></span>

### <span data-ttu-id="59070-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59070-116">-DefaultProfile</span></span>
<span data-ttu-id="59070-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="59070-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59070-118">-Force</span><span class="sxs-lookup"><span data-stu-id="59070-118">-Force</span></span>
<span data-ttu-id="59070-119">리소스를 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="59070-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59070-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59070-120">-InputObject</span></span>
<span data-ttu-id="59070-121">서비스 엔드포인트 정책 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="59070-121">The service endpoint policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59070-122">-Name</span><span class="sxs-lookup"><span data-stu-id="59070-122">-Name</span></span>
<span data-ttu-id="59070-123">서비스 엔드포인트 정책의 이름</span><span class="sxs-lookup"><span data-stu-id="59070-123">The name of the service endpoint policy</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59070-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="59070-124">-PassThru</span></span>
<span data-ttu-id="59070-125">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="59070-125">Returns an object representing the item with which you are working.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59070-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59070-126">-ResourceGroupName</span></span>
<span data-ttu-id="59070-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59070-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59070-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="59070-128">-ResourceId</span></span>
<span data-ttu-id="59070-129">서비스 엔드포인트 정책의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="59070-129">The ID of service endpoint policy.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59070-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="59070-130">-Confirm</span></span>
<span data-ttu-id="59070-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="59070-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59070-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59070-132">-WhatIf</span></span>
<span data-ttu-id="59070-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="59070-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59070-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="59070-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59070-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59070-135">CommonParameters</span></span>
<span data-ttu-id="59070-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="59070-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59070-137">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="59070-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59070-138">입력</span><span class="sxs-lookup"><span data-stu-id="59070-138">INPUTS</span></span>

### <span data-ttu-id="59070-139">System.String</span><span class="sxs-lookup"><span data-stu-id="59070-139">System.String</span></span>

### <span data-ttu-id="59070-140">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="59070-140">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="59070-141">출력</span><span class="sxs-lookup"><span data-stu-id="59070-141">OUTPUTS</span></span>

### <span data-ttu-id="59070-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="59070-142">System.Boolean</span></span>

## <span data-ttu-id="59070-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="59070-143">NOTES</span></span>

## <span data-ttu-id="59070-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="59070-144">RELATED LINKS</span></span>

[<span data-ttu-id="59070-145">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="59070-145">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="59070-146">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="59070-146">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="59070-147">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="59070-147">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
