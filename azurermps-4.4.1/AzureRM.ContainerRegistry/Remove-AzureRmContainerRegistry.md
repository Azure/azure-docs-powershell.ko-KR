---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistry.md
ms.openlocfilehash: 5a5ea87044c18e82f4c17294356a35adb254eee4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527708"
---
# <span data-ttu-id="d8d43-101">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d8d43-101">Remove-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="d8d43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8d43-102">SYNOPSIS</span></span>
<span data-ttu-id="d8d43-103">컨테이너 레지스트리를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8d43-103">Removes a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8d43-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d8d43-104">SYNTAX</span></span>

### <span data-ttu-id="d8d43-105">NameResourceGroupParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="d8d43-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8d43-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8d43-106">RegistryObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistry -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8d43-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d8d43-107">DESCRIPTION</span></span>
<span data-ttu-id="d8d43-108">**AzureRmContainerRegistry** cmdlet에서는 컨테이너 레지스트리를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8d43-108">The **Remove-AzureRmContainerRegistry** cmdlet removes a container registry.</span></span>

## <span data-ttu-id="d8d43-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d8d43-109">EXAMPLES</span></span>

### <span data-ttu-id="d8d43-110">예제 1: 지정 된 컨테이너 레지스트리 제거</span><span class="sxs-lookup"><span data-stu-id="d8d43-110">Example 1: Remove a specified container registry</span></span>
```
PS C:\>Remove-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"
```

<span data-ttu-id="d8d43-111">이 명령은 지정 된 컨테이너 레지스트리를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8d43-111">This command removes the specified container registry.</span></span>

## <span data-ttu-id="d8d43-112">변수</span><span class="sxs-lookup"><span data-stu-id="d8d43-112">PARAMETERS</span></span>

### <span data-ttu-id="d8d43-113">-이름</span><span class="sxs-lookup"><span data-stu-id="d8d43-113">-Name</span></span>
<span data-ttu-id="d8d43-114">컨테이너 레지스트리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d8d43-114">Container Registry Name.</span></span>

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

### <span data-ttu-id="d8d43-115">-레지스트리</span><span class="sxs-lookup"><span data-stu-id="d8d43-115">-Registry</span></span>
<span data-ttu-id="d8d43-116">컨테이너 레지스트리 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d8d43-116">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8d43-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8d43-117">-ResourceGroupName</span></span>
<span data-ttu-id="d8d43-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d8d43-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="d8d43-119">-확인</span><span class="sxs-lookup"><span data-stu-id="d8d43-119">-Confirm</span></span>
<span data-ttu-id="d8d43-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8d43-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8d43-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8d43-121">-WhatIf</span></span>
<span data-ttu-id="d8d43-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d8d43-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8d43-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d8d43-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8d43-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8d43-124">-DefaultProfile</span></span>
<span data-ttu-id="d8d43-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d8d43-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8d43-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8d43-126">CommonParameters</span></span>
<span data-ttu-id="d8d43-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8d43-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8d43-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8d43-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8d43-129">입력</span><span class="sxs-lookup"><span data-stu-id="d8d43-129">INPUTS</span></span>

### <span data-ttu-id="d8d43-130">PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d8d43-130">PSContainerRegistry</span></span>
<span data-ttu-id="d8d43-131">' Registry ' 매개 변수는 파이프라인에서 ' PSContainerRegistry ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8d43-131">Parameter 'Registry' accepts value of type 'PSContainerRegistry' from the pipeline</span></span>

## <span data-ttu-id="d8d43-132">출력</span><span class="sxs-lookup"><span data-stu-id="d8d43-132">OUTPUTS</span></span>

### <span data-ttu-id="d8d43-133">않아야</span><span class="sxs-lookup"><span data-stu-id="d8d43-133">None</span></span>

## <span data-ttu-id="d8d43-134">상속자</span><span class="sxs-lookup"><span data-stu-id="d8d43-134">NOTES</span></span>

## <span data-ttu-id="d8d43-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d8d43-135">RELATED LINKS</span></span>

[<span data-ttu-id="d8d43-136">새로운 AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d8d43-136">New-AzureRmContainerRegistry</span></span>](./New-AzureRmContainerRegistry.md)

[<span data-ttu-id="d8d43-137">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d8d43-137">Get-AzureRmContainerRegistry</span></span>](./Get-AzureRmContainerRegistry.md)

[<span data-ttu-id="d8d43-138">업데이트-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d8d43-138">Update-AzureRmContainerRegistry</span></span>](./Update-AzureRmContainerRegistry.md)

