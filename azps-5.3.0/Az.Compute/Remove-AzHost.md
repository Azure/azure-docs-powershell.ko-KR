---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHost.md
ms.openlocfilehash: 0d3f3a34257ad32c8b606b99c3f7170fb15684b0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496006"
---
# <span data-ttu-id="308ab-101">Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="308ab-101">Remove-AzHost</span></span>

## <span data-ttu-id="308ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="308ab-102">SYNOPSIS</span></span>
<span data-ttu-id="308ab-103">호스트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="308ab-103">Removes a host.</span></span>

## <span data-ttu-id="308ab-104">구문</span><span class="sxs-lookup"><span data-stu-id="308ab-104">SYNTAX</span></span>

### <span data-ttu-id="308ab-105">DefaultParameter(기본값)</span><span class="sxs-lookup"><span data-stu-id="308ab-105">DefaultParameter (Default)</span></span>
```
Remove-AzHost [-ResourceGroupName] <String> [-HostGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="308ab-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="308ab-106">ResourceIdParameter</span></span>
```
Remove-AzHost [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="308ab-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="308ab-107">ObjectParameter</span></span>
```
Remove-AzHost [-InputObject] <PSHost> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="308ab-108">설명</span><span class="sxs-lookup"><span data-stu-id="308ab-108">DESCRIPTION</span></span>
<span data-ttu-id="308ab-109">이 cmdlet은 호스트를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="308ab-109">This cmdlet will delete a Host</span></span>

## <span data-ttu-id="308ab-110">예제</span><span class="sxs-lookup"><span data-stu-id="308ab-110">EXAMPLES</span></span>

### <span data-ttu-id="308ab-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="308ab-111">Example 1</span></span>
```
PS C:\> Get-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName | Remove-AzHost
```

<span data-ttu-id="308ab-112">이 명령은 주어진 호스트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="308ab-112">This command gets and removes the given host.</span></span>

### <span data-ttu-id="308ab-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="308ab-113">Example 2</span></span>
```
PS C:\> Remove-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName
```

<span data-ttu-id="308ab-114">이 명령은 주어진 호스트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="308ab-114">This command removes the given host.</span></span>

## <span data-ttu-id="308ab-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="308ab-115">PARAMETERS</span></span>

### <span data-ttu-id="308ab-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="308ab-116">-AsJob</span></span>
<span data-ttu-id="308ab-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="308ab-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="308ab-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="308ab-118">-DefaultProfile</span></span>
<span data-ttu-id="308ab-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="308ab-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="308ab-120">-HostGroupName</span><span class="sxs-lookup"><span data-stu-id="308ab-120">-HostGroupName</span></span>
<span data-ttu-id="308ab-121">호스트 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="308ab-121">The name of the host group.</span></span>

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

### <span data-ttu-id="308ab-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="308ab-122">-InputObject</span></span>
<span data-ttu-id="308ab-123">호스트의 로컬 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="308ab-123">The local object of the host.</span></span>

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

### <span data-ttu-id="308ab-124">-Name</span><span class="sxs-lookup"><span data-stu-id="308ab-124">-Name</span></span>
<span data-ttu-id="308ab-125">호스트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="308ab-125">The name of the host.</span></span>

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

### <span data-ttu-id="308ab-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="308ab-126">-ResourceGroupName</span></span>
<span data-ttu-id="308ab-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="308ab-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="308ab-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="308ab-128">-ResourceId</span></span>
<span data-ttu-id="308ab-129">리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="308ab-129">The ID of the resource.</span></span>

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

### <span data-ttu-id="308ab-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="308ab-130">-Confirm</span></span>
<span data-ttu-id="308ab-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="308ab-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="308ab-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="308ab-132">-WhatIf</span></span>
<span data-ttu-id="308ab-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="308ab-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="308ab-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="308ab-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="308ab-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="308ab-135">CommonParameters</span></span>
<span data-ttu-id="308ab-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="308ab-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="308ab-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="308ab-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="308ab-138">입력</span><span class="sxs-lookup"><span data-stu-id="308ab-138">INPUTS</span></span>

### <span data-ttu-id="308ab-139">System.String</span><span class="sxs-lookup"><span data-stu-id="308ab-139">System.String</span></span>

### <span data-ttu-id="308ab-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span><span class="sxs-lookup"><span data-stu-id="308ab-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span></span>

## <span data-ttu-id="308ab-141">출력</span><span class="sxs-lookup"><span data-stu-id="308ab-141">OUTPUTS</span></span>

### <span data-ttu-id="308ab-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="308ab-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="308ab-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="308ab-143">NOTES</span></span>

## <span data-ttu-id="308ab-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="308ab-144">RELATED LINKS</span></span>
