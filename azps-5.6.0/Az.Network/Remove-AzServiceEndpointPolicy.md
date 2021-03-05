---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicy.md
ms.openlocfilehash: 95da37a36c8a97bf507ec8d191728b34a88a25a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006144"
---
# <span data-ttu-id="bcfbd-101">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="bcfbd-101">Remove-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="bcfbd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bcfbd-102">SYNOPSIS</span></span>
<span data-ttu-id="bcfbd-103">서비스 엔드포인트 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="bcfbd-103">Removes a service endpoint policy.</span></span>

## <span data-ttu-id="bcfbd-104">구문</span><span class="sxs-lookup"><span data-stu-id="bcfbd-104">SYNTAX</span></span>

### <span data-ttu-id="bcfbd-105">RemoveByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="bcfbd-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzServiceEndpointPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bcfbd-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bcfbd-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzServiceEndpointPolicy -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bcfbd-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bcfbd-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzServiceEndpointPolicy -InputObject <PSServiceEndpointPolicy> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bcfbd-108">설명</span><span class="sxs-lookup"><span data-stu-id="bcfbd-108">DESCRIPTION</span></span>
<span data-ttu-id="bcfbd-109">**Remove-AzServiceEndpointPolicy** cmdlet은 서비스 엔드포인트 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="bcfbd-109">The **Remove-AzServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="bcfbd-110">예제</span><span class="sxs-lookup"><span data-stu-id="bcfbd-110">EXAMPLES</span></span>

### <span data-ttu-id="bcfbd-111">예제 1: 이름을 사용하여 서비스 엔드포인트 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="bcfbd-111">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzServiceEndpointPolicy -Name "Policy1" -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="bcfbd-112">이 명령은 이름 "resourcegroup1"을 사용하여 resourcegroup에 속하는 Policy1 이름으로 서비스 엔드포인트 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="bcfbd-112">This command removes a service endpoint policy with name Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

### <span data-ttu-id="bcfbd-113">예제 2: 입력 개체를 사용하여 서비스 엔드포인트 정책 제거</span><span class="sxs-lookup"><span data-stu-id="bcfbd-113">Example 2: Remove a service endpoint policy using input object</span></span>
```
Remove-AzServiceEndpointPolicy -InputObject $Policy1 -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="bcfbd-114">이 명령은 이름 "resourcegroup1"을 사용하여 리소스 그룹에 속하는 서비스 엔드포인트 정책 개체 Policy1을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="bcfbd-114">This command removes a service endpoint policy object Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

## <span data-ttu-id="bcfbd-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="bcfbd-115">PARAMETERS</span></span>

### <span data-ttu-id="bcfbd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcfbd-116">-DefaultProfile</span></span>
<span data-ttu-id="bcfbd-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bcfbd-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bcfbd-118">-Force</span><span class="sxs-lookup"><span data-stu-id="bcfbd-118">-Force</span></span>
<span data-ttu-id="bcfbd-119">리소스를 덮어 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bcfbd-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="bcfbd-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bcfbd-120">-InputObject</span></span>
<span data-ttu-id="bcfbd-121">서비스 엔드포인트 정책 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="bcfbd-121">The service endpoint policy object.</span></span>

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

### <span data-ttu-id="bcfbd-122">-Name</span><span class="sxs-lookup"><span data-stu-id="bcfbd-122">-Name</span></span>
<span data-ttu-id="bcfbd-123">서비스 엔드포인트 정책의 이름</span><span class="sxs-lookup"><span data-stu-id="bcfbd-123">The name of the service endpoint policy</span></span>

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

### <span data-ttu-id="bcfbd-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bcfbd-124">-PassThru</span></span>
<span data-ttu-id="bcfbd-125">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="bcfbd-125">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="bcfbd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcfbd-126">-ResourceGroupName</span></span>
<span data-ttu-id="bcfbd-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bcfbd-127">The resource group name.</span></span>

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

### <span data-ttu-id="bcfbd-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bcfbd-128">-ResourceId</span></span>
<span data-ttu-id="bcfbd-129">서비스 엔드포인트 정책의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="bcfbd-129">The ID of service endpoint policy.</span></span>

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

### <span data-ttu-id="bcfbd-130">-확인</span><span class="sxs-lookup"><span data-stu-id="bcfbd-130">-Confirm</span></span>
<span data-ttu-id="bcfbd-131">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bcfbd-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcfbd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcfbd-132">-WhatIf</span></span>
<span data-ttu-id="bcfbd-133">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="bcfbd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcfbd-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bcfbd-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcfbd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcfbd-135">CommonParameters</span></span>
<span data-ttu-id="bcfbd-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bcfbd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcfbd-137">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="bcfbd-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcfbd-138">입력</span><span class="sxs-lookup"><span data-stu-id="bcfbd-138">INPUTS</span></span>

### <span data-ttu-id="bcfbd-139">System.String</span><span class="sxs-lookup"><span data-stu-id="bcfbd-139">System.String</span></span>

### <span data-ttu-id="bcfbd-140">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="bcfbd-140">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="bcfbd-141">출력</span><span class="sxs-lookup"><span data-stu-id="bcfbd-141">OUTPUTS</span></span>

### <span data-ttu-id="bcfbd-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bcfbd-142">System.Boolean</span></span>

## <span data-ttu-id="bcfbd-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bcfbd-143">NOTES</span></span>

## <span data-ttu-id="bcfbd-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bcfbd-144">RELATED LINKS</span></span>

[<span data-ttu-id="bcfbd-145">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="bcfbd-145">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="bcfbd-146">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="bcfbd-146">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="bcfbd-147">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="bcfbd-147">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
