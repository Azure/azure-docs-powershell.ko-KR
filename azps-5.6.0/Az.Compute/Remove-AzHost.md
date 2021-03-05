---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHost.md
ms.openlocfilehash: 21c623187e72406d1120e225bf567a48bb2e6f30
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983312"
---
# <span data-ttu-id="5d0d1-101">Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="5d0d1-101">Remove-AzHost</span></span>

## <span data-ttu-id="5d0d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d0d1-102">SYNOPSIS</span></span>
<span data-ttu-id="5d0d1-103">호스트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="5d0d1-103">Removes a host.</span></span>

## <span data-ttu-id="5d0d1-104">구문</span><span class="sxs-lookup"><span data-stu-id="5d0d1-104">SYNTAX</span></span>

### <span data-ttu-id="5d0d1-105">DefaultParameter(기본값)</span><span class="sxs-lookup"><span data-stu-id="5d0d1-105">DefaultParameter (Default)</span></span>
```
Remove-AzHost [-ResourceGroupName] <String> [-HostGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d0d1-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="5d0d1-106">ResourceIdParameter</span></span>
```
Remove-AzHost [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5d0d1-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="5d0d1-107">ObjectParameter</span></span>
```
Remove-AzHost [-InputObject] <PSHost> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5d0d1-108">설명</span><span class="sxs-lookup"><span data-stu-id="5d0d1-108">DESCRIPTION</span></span>
<span data-ttu-id="5d0d1-109">이 cmdlet은 호스트를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="5d0d1-109">This cmdlet will delete a Host</span></span>

## <span data-ttu-id="5d0d1-110">예제</span><span class="sxs-lookup"><span data-stu-id="5d0d1-110">EXAMPLES</span></span>

### <span data-ttu-id="5d0d1-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="5d0d1-111">Example 1</span></span>
```
PS C:\> Get-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName | Remove-AzHost
```

<span data-ttu-id="5d0d1-112">이 명령은 주어진 호스트를 얻게 하여 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="5d0d1-112">This command gets and removes the given host.</span></span>

### <span data-ttu-id="5d0d1-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="5d0d1-113">Example 2</span></span>
```
PS C:\> Remove-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName
```

<span data-ttu-id="5d0d1-114">이 명령은 주어진 호스트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="5d0d1-114">This command removes the given host.</span></span>

## <span data-ttu-id="5d0d1-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="5d0d1-115">PARAMETERS</span></span>

### <span data-ttu-id="5d0d1-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5d0d1-116">-AsJob</span></span>
<span data-ttu-id="5d0d1-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="5d0d1-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5d0d1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d0d1-118">-DefaultProfile</span></span>
<span data-ttu-id="5d0d1-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5d0d1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d0d1-120">-HostGroupName</span><span class="sxs-lookup"><span data-stu-id="5d0d1-120">-HostGroupName</span></span>
<span data-ttu-id="5d0d1-121">호스트 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5d0d1-121">The name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d0d1-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5d0d1-122">-InputObject</span></span>
<span data-ttu-id="5d0d1-123">호스트의 로컬 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="5d0d1-123">The local object of the host.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSHost
Parameter Sets: ObjectParameter
Aliases: Host

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d0d1-124">-Name</span><span class="sxs-lookup"><span data-stu-id="5d0d1-124">-Name</span></span>
<span data-ttu-id="5d0d1-125">호스트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5d0d1-125">The name of the host.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: HostName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d0d1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d0d1-126">-ResourceGroupName</span></span>
<span data-ttu-id="5d0d1-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5d0d1-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d0d1-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5d0d1-128">-ResourceId</span></span>
<span data-ttu-id="5d0d1-129">리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5d0d1-129">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d0d1-130">-확인</span><span class="sxs-lookup"><span data-stu-id="5d0d1-130">-Confirm</span></span>
<span data-ttu-id="5d0d1-131">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d0d1-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d0d1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d0d1-132">-WhatIf</span></span>
<span data-ttu-id="5d0d1-133">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="5d0d1-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d0d1-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5d0d1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d0d1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d0d1-135">CommonParameters</span></span>
<span data-ttu-id="5d0d1-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5d0d1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d0d1-137">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5d0d1-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d0d1-138">입력</span><span class="sxs-lookup"><span data-stu-id="5d0d1-138">INPUTS</span></span>

### <span data-ttu-id="5d0d1-139">System.String</span><span class="sxs-lookup"><span data-stu-id="5d0d1-139">System.String</span></span>

### <span data-ttu-id="5d0d1-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span><span class="sxs-lookup"><span data-stu-id="5d0d1-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span></span>

## <span data-ttu-id="5d0d1-141">출력</span><span class="sxs-lookup"><span data-stu-id="5d0d1-141">OUTPUTS</span></span>

### <span data-ttu-id="5d0d1-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="5d0d1-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="5d0d1-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5d0d1-143">NOTES</span></span>

## <span data-ttu-id="5d0d1-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5d0d1-144">RELATED LINKS</span></span>
