---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicy.md
ms.openlocfilehash: 207a07186cd7284059e0824da1f86afbc22873f5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056156"
---
# <span data-ttu-id="d19f7-101">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="d19f7-101">Remove-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="d19f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d19f7-102">SYNOPSIS</span></span>
<span data-ttu-id="d19f7-103">서비스 끝점 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d19f7-103">Removes a service endpoint policy.</span></span>

## <span data-ttu-id="d19f7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d19f7-104">SYNTAX</span></span>

### <span data-ttu-id="d19f7-105">RemoveByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="d19f7-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzServiceEndpointPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d19f7-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d19f7-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzServiceEndpointPolicy -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d19f7-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d19f7-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzServiceEndpointPolicy -InputObject <PSServiceEndpointPolicy> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d19f7-108">설명은</span><span class="sxs-lookup"><span data-stu-id="d19f7-108">DESCRIPTION</span></span>
<span data-ttu-id="d19f7-109">**AzServiceEndpointPolicy** cmdlet은 서비스 끝점 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d19f7-109">The **Remove-AzServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="d19f7-110">예제의</span><span class="sxs-lookup"><span data-stu-id="d19f7-110">EXAMPLES</span></span>

### <span data-ttu-id="d19f7-111">예제 1: 이름을 사용 하 여 서비스 끝점 정책 제거</span><span class="sxs-lookup"><span data-stu-id="d19f7-111">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzServiceEndpointPolicy -Name "Policy1" -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="d19f7-112">이 명령은 이름이 "resourcegroup1" 인 resourcegroup에 속하는 이름 Policy1 인 서비스 끝점 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d19f7-112">This command removes a service endpoint policy with name Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

### <span data-ttu-id="d19f7-113">예제 2: 입력 개체를 사용 하 여 서비스 끝점 정책 제거</span><span class="sxs-lookup"><span data-stu-id="d19f7-113">Example 2: Remove a service endpoint policy using input object</span></span>
```
Remove-AzServiceEndpointPolicy -InputObject $Policy1 -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="d19f7-114">이 명령은 이름이 "resourcegroup1" 인 resourcegroup에 속하는 서비스 끝점 정책 개체 Policy1를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d19f7-114">This command removes a service endpoint policy object Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

## <span data-ttu-id="d19f7-115">변수</span><span class="sxs-lookup"><span data-stu-id="d19f7-115">PARAMETERS</span></span>

### <span data-ttu-id="d19f7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d19f7-116">-DefaultProfile</span></span>
<span data-ttu-id="d19f7-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d19f7-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d19f7-118">-Force</span><span class="sxs-lookup"><span data-stu-id="d19f7-118">-Force</span></span>
<span data-ttu-id="d19f7-119">리소스를 덮어쓰려고 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="d19f7-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="d19f7-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d19f7-120">-InputObject</span></span>
<span data-ttu-id="d19f7-121">서비스 끝점 정책 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d19f7-121">The service endpoint policy object.</span></span>

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

### <span data-ttu-id="d19f7-122">-이름</span><span class="sxs-lookup"><span data-stu-id="d19f7-122">-Name</span></span>
<span data-ttu-id="d19f7-123">서비스 끝점 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d19f7-123">The name of the service endpoint policy</span></span>

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

### <span data-ttu-id="d19f7-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d19f7-124">-PassThru</span></span>
<span data-ttu-id="d19f7-125">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d19f7-125">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="d19f7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d19f7-126">-ResourceGroupName</span></span>
<span data-ttu-id="d19f7-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d19f7-127">The resource group name.</span></span>

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

### <span data-ttu-id="d19f7-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d19f7-128">-ResourceId</span></span>
<span data-ttu-id="d19f7-129">서비스 끝점 정책의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d19f7-129">The ID of service endpoint policy.</span></span>

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

### <span data-ttu-id="d19f7-130">-확인</span><span class="sxs-lookup"><span data-stu-id="d19f7-130">-Confirm</span></span>
<span data-ttu-id="d19f7-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d19f7-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d19f7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d19f7-132">-WhatIf</span></span>
<span data-ttu-id="d19f7-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d19f7-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d19f7-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d19f7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d19f7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d19f7-135">CommonParameters</span></span>
<span data-ttu-id="d19f7-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d19f7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d19f7-137">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d19f7-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d19f7-138">입력</span><span class="sxs-lookup"><span data-stu-id="d19f7-138">INPUTS</span></span>

### <span data-ttu-id="d19f7-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d19f7-139">System.String</span></span>

### <span data-ttu-id="d19f7-140">Microsoft. 네트워크. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="d19f7-140">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="d19f7-141">출력</span><span class="sxs-lookup"><span data-stu-id="d19f7-141">OUTPUTS</span></span>

### <span data-ttu-id="d19f7-142">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="d19f7-142">System.Boolean</span></span>

## <span data-ttu-id="d19f7-143">상속자</span><span class="sxs-lookup"><span data-stu-id="d19f7-143">NOTES</span></span>

## <span data-ttu-id="d19f7-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d19f7-144">RELATED LINKS</span></span>

[<span data-ttu-id="d19f7-145">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="d19f7-145">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="d19f7-146">새로운 AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="d19f7-146">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="d19f7-147">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="d19f7-147">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
