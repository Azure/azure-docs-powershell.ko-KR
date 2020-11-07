---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpPrefix.md
ms.openlocfilehash: 962c7d8f5120e0d6ae75d584edf261307bcefbee
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700128"
---
# <span data-ttu-id="69841-101">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="69841-101">Remove-AzPublicIpPrefix</span></span>

## <span data-ttu-id="69841-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69841-102">SYNOPSIS</span></span>
<span data-ttu-id="69841-103">공용 IP 접두사를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="69841-103">Removes a public IP prefix</span></span>

## <span data-ttu-id="69841-104">구문과</span><span class="sxs-lookup"><span data-stu-id="69841-104">SYNTAX</span></span>

### <span data-ttu-id="69841-105">RemoveByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="69841-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69841-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="69841-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzPublicIpPrefix -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69841-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="69841-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzPublicIpPrefix -InputObject <PSPublicIpPrefix> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69841-108">설명은</span><span class="sxs-lookup"><span data-stu-id="69841-108">DESCRIPTION</span></span>
<span data-ttu-id="69841-109">**AzPublicIpPrefix** cmdlet은 할당 된 공용 ip 주소가 없는 한 AZURE 공용 ip 접두사를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="69841-109">The **Remove-AzPublicIpPrefix** cmdlet removes an Azure public IP prefix as long as there are no public IP addresses allocated from it.</span></span>

## <span data-ttu-id="69841-110">예제의</span><span class="sxs-lookup"><span data-stu-id="69841-110">EXAMPLES</span></span>

### <span data-ttu-id="69841-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="69841-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName
```

<span data-ttu-id="69841-112">리소스 그룹의 이름이 $prefixName 인 공용 IP 접두사를 제거 $rgName</span><span class="sxs-lookup"><span data-stu-id="69841-112">Removes the public IP prefix with Name $prefixName from resource group $rgName</span></span>

## <span data-ttu-id="69841-113">변수</span><span class="sxs-lookup"><span data-stu-id="69841-113">PARAMETERS</span></span>

### <span data-ttu-id="69841-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="69841-114">-AsJob</span></span>
<span data-ttu-id="69841-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="69841-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="69841-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69841-116">-DefaultProfile</span></span>
<span data-ttu-id="69841-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="69841-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69841-118">-Force</span><span class="sxs-lookup"><span data-stu-id="69841-118">-Force</span></span>
<span data-ttu-id="69841-119">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="69841-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="69841-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69841-120">-InputObject</span></span>
<span data-ttu-id="69841-121">PublicIpPrefix 개체</span><span class="sxs-lookup"><span data-stu-id="69841-121">A PublicIpPrefix object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69841-122">-이름</span><span class="sxs-lookup"><span data-stu-id="69841-122">-Name</span></span>
<span data-ttu-id="69841-123">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="69841-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69841-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="69841-124">-PassThru</span></span>
<span data-ttu-id="69841-125">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="69841-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="69841-126">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="69841-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="69841-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69841-127">-ResourceGroupName</span></span>
<span data-ttu-id="69841-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="69841-128">The resource group name.</span></span>

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

### <span data-ttu-id="69841-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="69841-129">-ResourceId</span></span>
<span data-ttu-id="69841-130">제거할 리소스의 resourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="69841-130">The resourceId for the resource to remove</span></span>

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

### <span data-ttu-id="69841-131">-확인</span><span class="sxs-lookup"><span data-stu-id="69841-131">-Confirm</span></span>
<span data-ttu-id="69841-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="69841-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69841-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69841-133">-WhatIf</span></span>
<span data-ttu-id="69841-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="69841-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69841-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="69841-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69841-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69841-136">CommonParameters</span></span>
<span data-ttu-id="69841-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="69841-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69841-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69841-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69841-139">입력</span><span class="sxs-lookup"><span data-stu-id="69841-139">INPUTS</span></span>

### <span data-ttu-id="69841-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="69841-140">System.String</span></span>

### <span data-ttu-id="69841-141">PSPublicIpPrefix에 대 한.</span><span class="sxs-lookup"><span data-stu-id="69841-141">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="69841-142">출력</span><span class="sxs-lookup"><span data-stu-id="69841-142">OUTPUTS</span></span>

### <span data-ttu-id="69841-143">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="69841-143">System.Boolean</span></span>

## <span data-ttu-id="69841-144">상속자</span><span class="sxs-lookup"><span data-stu-id="69841-144">NOTES</span></span>

## <span data-ttu-id="69841-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="69841-145">RELATED LINKS</span></span>

[<span data-ttu-id="69841-146">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="69841-146">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="69841-147">새로운 AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="69841-147">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="69841-148">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="69841-148">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)