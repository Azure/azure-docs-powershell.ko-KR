---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerinstance/remove-azurermcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Remove-AzureRmContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Remove-AzureRmContainerGroup.md
ms.openlocfilehash: f1971f8bf0e7d8e779743739b8dd041effe3ba5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526219"
---
# <span data-ttu-id="8c73a-101">Remove-AzureRmContainerGroup</span><span class="sxs-lookup"><span data-stu-id="8c73a-101">Remove-AzureRmContainerGroup</span></span>

## <span data-ttu-id="8c73a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c73a-102">SYNOPSIS</span></span>
<span data-ttu-id="8c73a-103">컨테이너 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c73a-103">Removes a container group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c73a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8c73a-104">SYNTAX</span></span>

### <span data-ttu-id="8c73a-105">RemoveContainerGroupByResourceGroupAndNameParamSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="8c73a-105">RemoveContainerGroupByResourceGroupAndNameParamSet (Default)</span></span>
```
Remove-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c73a-106">RemoveContainerGroupByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="8c73a-106">RemoveContainerGroupByPSContainerGroupParamSet</span></span>
```
Remove-AzureRmContainerGroup -InputObject <PSContainerGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c73a-107">RemoveContainerGroupByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="8c73a-107">RemoveContainerGroupByResourceIdParamSet</span></span>
```
Remove-AzureRmContainerGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c73a-108">설명은</span><span class="sxs-lookup"><span data-stu-id="8c73a-108">DESCRIPTION</span></span>
<span data-ttu-id="8c73a-109">**제거-AzureRmContainerGroup** cmdlet은 컨테이너 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c73a-109">The **Remove-AzureRmContainerGroup** cmdlet removes a container group.</span></span>

## <span data-ttu-id="8c73a-110">예제의</span><span class="sxs-lookup"><span data-stu-id="8c73a-110">EXAMPLES</span></span>

### <span data-ttu-id="8c73a-111">예제 1: 컨테이너 그룹 제거</span><span class="sxs-lookup"><span data-stu-id="8c73a-111">Example 1: Removes a container group</span></span>
```
PS C:\> Remove-AzureRmContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer
```

<span data-ttu-id="8c73a-112">이 명령은 지정 된 컨테이너 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c73a-112">This command removes the specified container group.</span></span>

### <span data-ttu-id="8c73a-113">예제 2: 파이프를 기준으로 컨테이너 그룹 제거</span><span class="sxs-lookup"><span data-stu-id="8c73a-113">Example 2: Removes a container group by piping</span></span>
```
PS C:\> Get-AzureRmContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer | Remove-AzureRmContainerGroup
```

<span data-ttu-id="8c73a-114">이 명령은 파이프를 기준으로 컨테이너 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c73a-114">This command removes a container group by piping.</span></span>

### <span data-ttu-id="8c73a-115">예제 3: 리소스 Id를 기준으로 컨테이너 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c73a-115">Example 3: Removes a container group by resource Id.</span></span>
```
PS C:\> Find-AzureRmResource -ResourceGroupEquals MyResourceGroup -ResourceNameEquals MyContainer | Remove-AzureRmContainerGroup
```

<span data-ttu-id="8c73a-116">이 명령은 리소스 Id를 기준으로 컨테이너 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c73a-116">This command removes a container group by resource Id.</span></span>

## <span data-ttu-id="8c73a-117">변수</span><span class="sxs-lookup"><span data-stu-id="8c73a-117">PARAMETERS</span></span>

### <span data-ttu-id="8c73a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c73a-118">-DefaultProfile</span></span>
<span data-ttu-id="8c73a-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8c73a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c73a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8c73a-120">-InputObject</span></span>
<span data-ttu-id="8c73a-121">제거할 컨테이너 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="8c73a-121">The container group to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup
Parameter Sets: RemoveContainerGroupByPSContainerGroupParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c73a-122">-이름</span><span class="sxs-lookup"><span data-stu-id="8c73a-122">-Name</span></span>
<span data-ttu-id="8c73a-123">컨테이너 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8c73a-123">The container group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveContainerGroupByResourceGroupAndNameParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c73a-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8c73a-124">-PassThru</span></span>
<span data-ttu-id="8c73a-125">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="8c73a-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="8c73a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c73a-126">-ResourceGroupName</span></span>
<span data-ttu-id="8c73a-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8c73a-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveContainerGroupByResourceGroupAndNameParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c73a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c73a-128">-ResourceId</span></span>
<span data-ttu-id="8c73a-129">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="8c73a-129">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveContainerGroupByResourceIdParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c73a-130">-확인</span><span class="sxs-lookup"><span data-stu-id="8c73a-130">-Confirm</span></span>
<span data-ttu-id="8c73a-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c73a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c73a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c73a-132">-WhatIf</span></span>
<span data-ttu-id="8c73a-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8c73a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c73a-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8c73a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c73a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c73a-135">CommonParameters</span></span>
<span data-ttu-id="8c73a-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c73a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c73a-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c73a-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c73a-138">입력</span><span class="sxs-lookup"><span data-stu-id="8c73a-138">INPUTS</span></span>

### <span data-ttu-id="8c73a-139">ContainerInstance. PSContainerGroup/.</span><span class="sxs-lookup"><span data-stu-id="8c73a-139">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>
<span data-ttu-id="8c73a-140">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8c73a-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="8c73a-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8c73a-141">System.String</span></span>

## <span data-ttu-id="8c73a-142">출력</span><span class="sxs-lookup"><span data-stu-id="8c73a-142">OUTPUTS</span></span>

### <span data-ttu-id="8c73a-143">ContainerInstance. PSContainerGroup/.</span><span class="sxs-lookup"><span data-stu-id="8c73a-143">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="8c73a-144">상속자</span><span class="sxs-lookup"><span data-stu-id="8c73a-144">NOTES</span></span>

## <span data-ttu-id="8c73a-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8c73a-145">RELATED LINKS</span></span>
