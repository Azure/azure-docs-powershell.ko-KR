---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7F7D1F05-617C-4EC5-8FF5-D816E9148841
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/start-azurermvmss
schema: 2.0.0
ms.openlocfilehash: 2135b6244453cb7d958871c23b64016404d02502
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882650"
---
# <span data-ttu-id="c4de0-101">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c4de0-101">Start-AzureRmVmss</span></span>

## <span data-ttu-id="c4de0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4de0-102">SYNOPSIS</span></span>
<span data-ttu-id="c4de0-103">Vmss 또는 VMSS 내의 가상 컴퓨터 집합을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4de0-103">Starts the VMSS or a set of virtual machines within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4de0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c4de0-104">SYNTAX</span></span>

```
Start-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4de0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c4de0-105">DESCRIPTION</span></span>
<span data-ttu-id="c4de0-106">**AzureRmVmss** CMDLET은 vmss (가상 컴퓨터 크기 집합) 또는 가상 컴퓨터 집합 내의 모든 가상 컴퓨터를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4de0-106">The **Start-AzureRmVmss** cmdlet starts all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="c4de0-107">*InstanceId* 매개 변수를 사용 하 여 가상 컴퓨터 집합을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c4de0-107">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="c4de0-108">예제의</span><span class="sxs-lookup"><span data-stu-id="c4de0-108">EXAMPLES</span></span>

### <span data-ttu-id="c4de0-109">예제 1: VMSS 내에서 가상 컴퓨터의 특정 집합 시작</span><span class="sxs-lookup"><span data-stu-id="c4de0-109">Example 1: Start a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzureRmVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"-InstanceId "0", "1"
```

<span data-ttu-id="c4de0-110">이 명령은 ContosoVMSS 이라는 VMSS에 속하는 인스턴스 ID 문자열 배열에 지정 된 가상 컴퓨터의 특정 집합을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4de0-110">This command starts a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="c4de0-111">예제 2: VMSS 내의 모든 가상 컴퓨터 시작</span><span class="sxs-lookup"><span data-stu-id="c4de0-111">Example 2: Start all virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzureRmVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="c4de0-112">이 명령은 ContosoVMSS 이라는 VMSS에 속하는 모든 가상 컴퓨터를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4de0-112">This command starts all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="c4de0-113">변수</span><span class="sxs-lookup"><span data-stu-id="c4de0-113">PARAMETERS</span></span>

### <span data-ttu-id="c4de0-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c4de0-114">-AsJob</span></span>
<span data-ttu-id="c4de0-115">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4de0-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="c4de0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4de0-116">-DefaultProfile</span></span>
<span data-ttu-id="c4de0-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c4de0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4de0-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="c4de0-118">-InstanceId</span></span>
<span data-ttu-id="c4de0-119">Cmdlet이 시작 되는 인스턴스의 ID 또는 식별자를 문자열 배열로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4de0-119">Specifies, as a string array, the ID or IDs of the instances that cmdlet starts.</span></span>
<span data-ttu-id="c4de0-120">예를 들면 다음과 같습니다. `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="c4de0-120">For instance: `-InstanceId "0", "3"`</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4de0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4de0-121">-ResourceGroupName</span></span>
<span data-ttu-id="c4de0-122">VMSS의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4de0-122">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="c4de0-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="c4de0-123">-VMScaleSetName</span></span>
<span data-ttu-id="c4de0-124">이 cmdlet이 가상 컴퓨터를 시작 하는 VMSS의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4de0-124">Specifies the name of the VMSS that this cmdlet starts the virtual machines.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4de0-125">-확인</span><span class="sxs-lookup"><span data-stu-id="c4de0-125">-Confirm</span></span>
<span data-ttu-id="c4de0-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4de0-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4de0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4de0-127">-WhatIf</span></span>
<span data-ttu-id="c4de0-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c4de0-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c4de0-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c4de0-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4de0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4de0-130">CommonParameters</span></span>
<span data-ttu-id="c4de0-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4de0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4de0-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4de0-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4de0-133">입력</span><span class="sxs-lookup"><span data-stu-id="c4de0-133">INPUTS</span></span>

### <span data-ttu-id="c4de0-134">않아야</span><span class="sxs-lookup"><span data-stu-id="c4de0-134">None</span></span>
<span data-ttu-id="c4de0-135">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c4de0-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c4de0-136">출력</span><span class="sxs-lookup"><span data-stu-id="c4de0-136">OUTPUTS</span></span>

###  
<span data-ttu-id="c4de0-137">이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c4de0-137">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="c4de0-138">상속자</span><span class="sxs-lookup"><span data-stu-id="c4de0-138">NOTES</span></span>

## <span data-ttu-id="c4de0-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c4de0-139">RELATED LINKS</span></span>

[<span data-ttu-id="c4de0-140">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c4de0-140">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="c4de0-141">새로운 AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c4de0-141">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="c4de0-142">제거-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c4de0-142">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="c4de0-143">다시 시작-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c4de0-143">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="c4de0-144">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c4de0-144">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="c4de0-145">중지-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c4de0-145">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="c4de0-146">업데이트-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c4de0-146">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)

