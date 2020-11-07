---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/remove-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistry.md
ms.openlocfilehash: 2235e533e999fedbb06b79548bf4e2ce8de3586a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703876"
---
# <span data-ttu-id="1bedb-101">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1bedb-101">Remove-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="1bedb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1bedb-102">SYNOPSIS</span></span>
<span data-ttu-id="1bedb-103">컨테이너 레지스트리를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bedb-103">Removes a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1bedb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1bedb-104">SYNTAX</span></span>

### <span data-ttu-id="1bedb-105">NameResourceGroupParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="1bedb-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bedb-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1bedb-106">RegistryObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistry -Registry <PSContainerRegistry> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bedb-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1bedb-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmContainerRegistry -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1bedb-108">설명은</span><span class="sxs-lookup"><span data-stu-id="1bedb-108">DESCRIPTION</span></span>
<span data-ttu-id="1bedb-109">Remove-AzureRmContainerRegistry cmdlet은 컨테이너 레지스트리를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bedb-109">The Remove-AzureRmContainerRegistry cmdlet removes a container registry.</span></span>

## <span data-ttu-id="1bedb-110">예제의</span><span class="sxs-lookup"><span data-stu-id="1bedb-110">EXAMPLES</span></span>

### <span data-ttu-id="1bedb-111">예제 1: 지정 된 컨테이너 레지스트리 제거</span><span class="sxs-lookup"><span data-stu-id="1bedb-111">Example 1: Remove a specified container registry</span></span>
```powershell
PS C:\>Remove-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"
```

<span data-ttu-id="1bedb-112">이 명령은 지정 된 컨테이너 레지스트리를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bedb-112">This command removes the specified container registry.</span></span>

## <span data-ttu-id="1bedb-113">변수</span><span class="sxs-lookup"><span data-stu-id="1bedb-113">PARAMETERS</span></span>

### <span data-ttu-id="1bedb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bedb-114">-DefaultProfile</span></span>
<span data-ttu-id="1bedb-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="1bedb-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1bedb-116">-이름</span><span class="sxs-lookup"><span data-stu-id="1bedb-116">-Name</span></span>
<span data-ttu-id="1bedb-117">컨테이너 레지스트리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1bedb-117">Container Registry Name.</span></span>

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

### <span data-ttu-id="1bedb-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1bedb-118">-PassThru</span></span>
<span data-ttu-id="1bedb-119">제거에 성공한 경우이 cmdlet이 true를 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1bedb-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="1bedb-120">-레지스트리</span><span class="sxs-lookup"><span data-stu-id="1bedb-120">-Registry</span></span>
<span data-ttu-id="1bedb-121">컨테이너 레지스트리 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="1bedb-121">Container Registry Object.</span></span>

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

### <span data-ttu-id="1bedb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bedb-122">-ResourceGroupName</span></span>
<span data-ttu-id="1bedb-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1bedb-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="1bedb-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1bedb-124">-ResourceId</span></span>
<span data-ttu-id="1bedb-125">컨테이너 레지스트리 리소스 id</span><span class="sxs-lookup"><span data-stu-id="1bedb-125">The container registry resource id</span></span>

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

### <span data-ttu-id="1bedb-126">-확인</span><span class="sxs-lookup"><span data-stu-id="1bedb-126">-Confirm</span></span>
<span data-ttu-id="1bedb-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bedb-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bedb-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bedb-128">-WhatIf</span></span>
<span data-ttu-id="1bedb-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1bedb-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1bedb-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1bedb-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bedb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bedb-131">CommonParameters</span></span>
<span data-ttu-id="1bedb-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bedb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bedb-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bedb-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bedb-134">입력</span><span class="sxs-lookup"><span data-stu-id="1bedb-134">INPUTS</span></span>

### <span data-ttu-id="1bedb-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1bedb-135">System.String</span></span>

## <span data-ttu-id="1bedb-136">출력</span><span class="sxs-lookup"><span data-stu-id="1bedb-136">OUTPUTS</span></span>

### <span data-ttu-id="1bedb-137">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="1bedb-137">System.Boolean</span></span>

## <span data-ttu-id="1bedb-138">상속자</span><span class="sxs-lookup"><span data-stu-id="1bedb-138">NOTES</span></span>

## <span data-ttu-id="1bedb-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1bedb-139">RELATED LINKS</span></span>

[<span data-ttu-id="1bedb-140">새로운 AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1bedb-140">New-AzureRmContainerRegistry</span></span>]()

[<span data-ttu-id="1bedb-141">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1bedb-141">Get-AzureRmContainerRegistry</span></span>]()

[<span data-ttu-id="1bedb-142">업데이트-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1bedb-142">Update-AzureRmContainerRegistry</span></span>]()

