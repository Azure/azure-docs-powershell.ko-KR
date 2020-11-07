---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/remove-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryReplication.md
ms.openlocfilehash: 824b3226b29ba381b9ed963bf6a21f4691c17733
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702740"
---
# <span data-ttu-id="2a28a-101">Remove-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="2a28a-101">Remove-AzureRmContainerRegistryReplication</span></span>

## <span data-ttu-id="2a28a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a28a-102">SYNOPSIS</span></span>
<span data-ttu-id="2a28a-103">컨테이너 레지스트리 복제를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a28a-103">Removes a container registry replication.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a28a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2a28a-104">SYNTAX</span></span>

### <span data-ttu-id="2a28a-105">NameResourceGroupParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="2a28a-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String>
 [-RegistryName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2a28a-106">ReplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a28a-106">ReplicationObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistryReplication -Replicatoin <PSContainerRegistryReplication> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a28a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a28a-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmContainerRegistryReplication -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a28a-108">설명은</span><span class="sxs-lookup"><span data-stu-id="2a28a-108">DESCRIPTION</span></span>
<span data-ttu-id="2a28a-109">Remove-AzureRmContainerRegistryReplication cmdlet은 컨테이너 레지스트리 복제를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a28a-109">The Remove-AzureRmContainerRegistryReplication cmdlet removes a container registry replication.</span></span>

## <span data-ttu-id="2a28a-110">예제의</span><span class="sxs-lookup"><span data-stu-id="2a28a-110">EXAMPLES</span></span>

### <span data-ttu-id="2a28a-111">예제 1: 컨테이너 레지스트리 복제를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a28a-111">Example 1: Removes a container registry replication.</span></span>
```powershell
PS C:\> Remove-AzureRmContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "replication001"
```

<span data-ttu-id="2a28a-112">컨테이너 레지스트리 복제를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a28a-112">Removes a container registry replication.</span></span>

## <span data-ttu-id="2a28a-113">변수</span><span class="sxs-lookup"><span data-stu-id="2a28a-113">PARAMETERS</span></span>

### <span data-ttu-id="2a28a-114">-확인</span><span class="sxs-lookup"><span data-stu-id="2a28a-114">-Confirm</span></span>
<span data-ttu-id="2a28a-115">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a28a-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a28a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a28a-116">-DefaultProfile</span></span>
<span data-ttu-id="2a28a-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2a28a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a28a-118">-이름</span><span class="sxs-lookup"><span data-stu-id="2a28a-118">-Name</span></span>
<span data-ttu-id="2a28a-119">컨테이너 레지스트리 복제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2a28a-119">Container Registry Replication Name.</span></span>
<span data-ttu-id="2a28a-120">위치 이름을 기본값으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a28a-120">Default to the location name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ReplicationName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a28a-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="2a28a-121">-RegistryName</span></span>
<span data-ttu-id="2a28a-122">컨테이너 레지스트리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2a28a-122">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a28a-123">-Replicatoin</span><span class="sxs-lookup"><span data-stu-id="2a28a-123">-Replicatoin</span></span>
<span data-ttu-id="2a28a-124">컨테이너 레지스트리 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="2a28a-124">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistryReplication
Parameter Sets: ReplicationObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a28a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a28a-125">-ResourceGroupName</span></span>
<span data-ttu-id="2a28a-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2a28a-126">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a28a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a28a-127">-ResourceId</span></span>
<span data-ttu-id="2a28a-128">컨테이너 레지스트리 복제 리소스 id</span><span class="sxs-lookup"><span data-stu-id="2a28a-128">The container registry replication resource id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a28a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a28a-129">-WhatIf</span></span>
<span data-ttu-id="2a28a-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2a28a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a28a-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2a28a-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a28a-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2a28a-132">-PassThru</span></span>
<span data-ttu-id="2a28a-133">제거에 성공한 경우이 cmdlet이 true를 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2a28a-133">Indicates that this cmdlet returns true if the removal was successful.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a28a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a28a-134">CommonParameters</span></span>
<span data-ttu-id="2a28a-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a28a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a28a-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a28a-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a28a-137">입력</span><span class="sxs-lookup"><span data-stu-id="2a28a-137">INPUTS</span></span>

### <span data-ttu-id="2a28a-138">ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="2a28a-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>
<span data-ttu-id="2a28a-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2a28a-139">System.String</span></span>

## <span data-ttu-id="2a28a-140">출력</span><span class="sxs-lookup"><span data-stu-id="2a28a-140">OUTPUTS</span></span>

### <span data-ttu-id="2a28a-141">System. 개체</span><span class="sxs-lookup"><span data-stu-id="2a28a-141">System.Object</span></span>

## <span data-ttu-id="2a28a-142">상속자</span><span class="sxs-lookup"><span data-stu-id="2a28a-142">NOTES</span></span>

## <span data-ttu-id="2a28a-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2a28a-143">RELATED LINKS</span></span>

[<span data-ttu-id="2a28a-144">새로운 AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="2a28a-144">New-AzureRmContainerRegistryReplication</span></span>](New-AzureRmContainerRegistryReplication.md)

[<span data-ttu-id="2a28a-145">Get-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="2a28a-145">Get-AzureRmContainerRegistryReplication</span></span>](Remove-AzureRmContainerRegistryReplication.md)

