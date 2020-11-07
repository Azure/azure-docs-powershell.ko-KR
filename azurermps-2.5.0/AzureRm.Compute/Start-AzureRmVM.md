---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/start-azurermvm
schema: 2.0.0
ms.openlocfilehash: 04110cb46d3f0ed0e5e09e6b12544b927cf6ae25
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881914"
---
# <span data-ttu-id="369e6-101">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="369e6-101">Start-AzureRmVM</span></span>

## <span data-ttu-id="369e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="369e6-102">SYNOPSIS</span></span>
<span data-ttu-id="369e6-103">Azure 가상 머신을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="369e6-103">Starts an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="369e6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="369e6-104">SYNTAX</span></span>

### <span data-ttu-id="369e6-105">ResourceGroupNameParameterSetName (기본값)</span><span class="sxs-lookup"><span data-stu-id="369e6-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzureRmVM [-Name] <String> [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="369e6-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="369e6-106">IdParameterSetName</span></span>
```
Start-AzureRmVM [-Name] <String> [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="369e6-107">설명은</span><span class="sxs-lookup"><span data-stu-id="369e6-107">DESCRIPTION</span></span>
<span data-ttu-id="369e6-108">**AzureRmVM** Cmdlet은 Azure 가상 머신을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="369e6-108">The **Start-AzureRmVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="369e6-109">예제의</span><span class="sxs-lookup"><span data-stu-id="369e6-109">EXAMPLES</span></span>

### <span data-ttu-id="369e6-110">예제 1: 가상 컴퓨터 시작</span><span class="sxs-lookup"><span data-stu-id="369e6-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="369e6-111">이 명령은 ResourceGroup11에서 VirtualMachine07 이라는 가상 컴퓨터를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="369e6-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="369e6-112">변수</span><span class="sxs-lookup"><span data-stu-id="369e6-112">PARAMETERS</span></span>

### <span data-ttu-id="369e6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="369e6-113">-AsJob</span></span>
<span data-ttu-id="369e6-114">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="369e6-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="369e6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="369e6-115">-DefaultProfile</span></span>
<span data-ttu-id="369e6-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="369e6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="369e6-117">-Id</span><span class="sxs-lookup"><span data-stu-id="369e6-117">-Id</span></span>
<span data-ttu-id="369e6-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="369e6-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="369e6-119">-이름</span><span class="sxs-lookup"><span data-stu-id="369e6-119">-Name</span></span>
<span data-ttu-id="369e6-120">가상 컴퓨터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="369e6-120">The virtual machine name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="369e6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="369e6-121">-ResourceGroupName</span></span>
<span data-ttu-id="369e6-122">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="369e6-122">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="369e6-123">-확인</span><span class="sxs-lookup"><span data-stu-id="369e6-123">-Confirm</span></span>
<span data-ttu-id="369e6-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="369e6-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="369e6-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="369e6-125">-WhatIf</span></span>
<span data-ttu-id="369e6-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="369e6-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="369e6-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="369e6-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="369e6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="369e6-128">CommonParameters</span></span>
<span data-ttu-id="369e6-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="369e6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="369e6-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="369e6-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="369e6-131">입력</span><span class="sxs-lookup"><span data-stu-id="369e6-131">INPUTS</span></span>

### <span data-ttu-id="369e6-132">않아야</span><span class="sxs-lookup"><span data-stu-id="369e6-132">None</span></span>
<span data-ttu-id="369e6-133">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="369e6-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="369e6-134">출력</span><span class="sxs-lookup"><span data-stu-id="369e6-134">OUTPUTS</span></span>

### <span data-ttu-id="369e6-135">PSComputeLongRunningOperation를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="369e6-135">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="369e6-136">상속자</span><span class="sxs-lookup"><span data-stu-id="369e6-136">NOTES</span></span>

## <span data-ttu-id="369e6-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="369e6-137">RELATED LINKS</span></span>

[<span data-ttu-id="369e6-138">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="369e6-138">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="369e6-139">새로운 AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="369e6-139">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="369e6-140">제거-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="369e6-140">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="369e6-141">다시 시작-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="369e6-141">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="369e6-142">중지-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="369e6-142">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="369e6-143">업데이트-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="369e6-143">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


