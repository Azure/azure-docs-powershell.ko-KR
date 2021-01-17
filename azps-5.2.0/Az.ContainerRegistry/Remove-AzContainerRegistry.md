---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistry.md
ms.openlocfilehash: d36e362f1782e3566bc0d2febd65aebd4c68220d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356258"
---
# <span data-ttu-id="732bd-101">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="732bd-101">Remove-AzContainerRegistry</span></span>

## <span data-ttu-id="732bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="732bd-102">SYNOPSIS</span></span>
<span data-ttu-id="732bd-103">컨테이너 레지스트리를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="732bd-103">Removes a container registry.</span></span>

## <span data-ttu-id="732bd-104">구문</span><span class="sxs-lookup"><span data-stu-id="732bd-104">SYNTAX</span></span>

### <span data-ttu-id="732bd-105">NameResourceGroupParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="732bd-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="732bd-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="732bd-106">RegistryObjectParameterSet</span></span>
```
Remove-AzContainerRegistry -Registry <PSContainerRegistry> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="732bd-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="732bd-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistry -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="732bd-108">설명</span><span class="sxs-lookup"><span data-stu-id="732bd-108">DESCRIPTION</span></span>
<span data-ttu-id="732bd-109">Remove-AzContainerRegistry cmdlet은 컨테이너 레지스트리를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="732bd-109">The Remove-AzContainerRegistry cmdlet removes a container registry.</span></span>

## <span data-ttu-id="732bd-110">예제</span><span class="sxs-lookup"><span data-stu-id="732bd-110">EXAMPLES</span></span>

### <span data-ttu-id="732bd-111">예제 1: 지정된 컨테이너 레지스트리 제거</span><span class="sxs-lookup"><span data-stu-id="732bd-111">Example 1: Remove a specified container registry</span></span>
```powershell
PS C:\>Remove-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"
```

<span data-ttu-id="732bd-112">이 명령은 지정된 컨테이너 레지스트리를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="732bd-112">This command removes the specified container registry.</span></span>

## <span data-ttu-id="732bd-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="732bd-113">PARAMETERS</span></span>

### <span data-ttu-id="732bd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="732bd-114">-DefaultProfile</span></span>
<span data-ttu-id="732bd-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="732bd-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="732bd-116">-Name</span><span class="sxs-lookup"><span data-stu-id="732bd-116">-Name</span></span>
<span data-ttu-id="732bd-117">Container Registry 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="732bd-117">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="732bd-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="732bd-118">-PassThru</span></span>
<span data-ttu-id="732bd-119">제거에 성공하면 이 cmdlet이 true를 반환하는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="732bd-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="732bd-120">-Registry</span><span class="sxs-lookup"><span data-stu-id="732bd-120">-Registry</span></span>
<span data-ttu-id="732bd-121">Container Registry 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="732bd-121">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="732bd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="732bd-122">-ResourceGroupName</span></span>
<span data-ttu-id="732bd-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="732bd-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="732bd-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="732bd-124">-ResourceId</span></span>
<span data-ttu-id="732bd-125">컨테이너 레지스트리 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="732bd-125">The container registry resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="732bd-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="732bd-126">-Confirm</span></span>
<span data-ttu-id="732bd-127">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="732bd-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="732bd-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="732bd-128">-WhatIf</span></span>
<span data-ttu-id="732bd-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="732bd-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="732bd-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="732bd-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="732bd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="732bd-131">CommonParameters</span></span>
<span data-ttu-id="732bd-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="732bd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="732bd-133">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="732bd-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="732bd-134">입력</span><span class="sxs-lookup"><span data-stu-id="732bd-134">INPUTS</span></span>

### <span data-ttu-id="732bd-135">System.String</span><span class="sxs-lookup"><span data-stu-id="732bd-135">System.String</span></span>

## <span data-ttu-id="732bd-136">출력</span><span class="sxs-lookup"><span data-stu-id="732bd-136">OUTPUTS</span></span>

### <span data-ttu-id="732bd-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="732bd-137">System.Boolean</span></span>

## <span data-ttu-id="732bd-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="732bd-138">NOTES</span></span>

## <span data-ttu-id="732bd-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="732bd-139">RELATED LINKS</span></span>

[<span data-ttu-id="732bd-140">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="732bd-140">New-AzContainerRegistry</span></span>]()

[<span data-ttu-id="732bd-141">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="732bd-141">Get-AzContainerRegistry</span></span>]()

[<span data-ttu-id="732bd-142">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="732bd-142">Update-AzContainerRegistry</span></span>]()

