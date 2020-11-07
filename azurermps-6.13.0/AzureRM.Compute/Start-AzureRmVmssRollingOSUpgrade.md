---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/start-azurermvmssrollingosupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Start-AzureRmVmssRollingOSUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Start-AzureRmVmssRollingOSUpgrade.md
ms.openlocfilehash: 239397bc91e42c55d400caf00a83619c4665bbce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703883"
---
# <span data-ttu-id="e16b3-101">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="e16b3-101">Start-AzureRmVmssRollingOSUpgrade</span></span>

## <span data-ttu-id="e16b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e16b3-102">SYNOPSIS</span></span>
<span data-ttu-id="e16b3-103">모든 가상 컴퓨터 크기 집합 인스턴스를 사용 가능한 최신 플랫폼 이미지 OS 버전으로 이동 하기 위해 롤링 업그레이드를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="e16b3-103">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e16b3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e16b3-104">SYNTAX</span></span>

```
Start-AzureRmVmssRollingOSUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e16b3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e16b3-105">DESCRIPTION</span></span>
<span data-ttu-id="e16b3-106">모든 가상 컴퓨터 크기 집합 인스턴스를 사용 가능한 최신 플랫폼 이미지 OS 버전으로 이동 하기 위해 롤링 업그레이드를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="e16b3-106">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>
<span data-ttu-id="e16b3-107">사용 가능한 최신 OS 버전을 이미 실행 중인 인스턴스는 영향을 받지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e16b3-107">Instances which are already running the latest available OS version are not affected.</span></span>

## <span data-ttu-id="e16b3-108">예제의</span><span class="sxs-lookup"><span data-stu-id="e16b3-108">EXAMPLES</span></span>

### <span data-ttu-id="e16b3-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="e16b3-109">Example 1</span></span>
```
PS C:\> Start-AzureRmVmssRollingOSUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="e16b3-110">이 명령은 리소스 그룹 "Group001"의 VM 확장 집합 "VMSS001"의 모든 vm 인스턴스에 대 한 롤링 업그레이드를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="e16b3-110">This command starts a rolling upgrade of all vm instances of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="e16b3-111">변수</span><span class="sxs-lookup"><span data-stu-id="e16b3-111">PARAMETERS</span></span>

### <span data-ttu-id="e16b3-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e16b3-112">-AsJob</span></span>
<span data-ttu-id="e16b3-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e16b3-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e16b3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e16b3-114">-DefaultProfile</span></span>
<span data-ttu-id="e16b3-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e16b3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e16b3-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e16b3-116">-ResourceGroupName</span></span>
<span data-ttu-id="e16b3-117">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e16b3-117">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e16b3-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="e16b3-118">-VMScaleSetName</span></span>
<span data-ttu-id="e16b3-119">VM 크기 집합의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e16b3-119">The name of the VM scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e16b3-120">-확인</span><span class="sxs-lookup"><span data-stu-id="e16b3-120">-Confirm</span></span>
<span data-ttu-id="e16b3-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e16b3-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e16b3-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e16b3-122">-WhatIf</span></span>
<span data-ttu-id="e16b3-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e16b3-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e16b3-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e16b3-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e16b3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e16b3-125">CommonParameters</span></span>
<span data-ttu-id="e16b3-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e16b3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e16b3-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e16b3-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e16b3-128">입력</span><span class="sxs-lookup"><span data-stu-id="e16b3-128">INPUTS</span></span>

### <span data-ttu-id="e16b3-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e16b3-129">System.String</span></span>

## <span data-ttu-id="e16b3-130">출력</span><span class="sxs-lookup"><span data-stu-id="e16b3-130">OUTPUTS</span></span>

### <span data-ttu-id="e16b3-131">PSOperationStatusResponse의. m a.</span><span class="sxs-lookup"><span data-stu-id="e16b3-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="e16b3-132">상속자</span><span class="sxs-lookup"><span data-stu-id="e16b3-132">NOTES</span></span>

## <span data-ttu-id="e16b3-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e16b3-133">RELATED LINKS</span></span>
