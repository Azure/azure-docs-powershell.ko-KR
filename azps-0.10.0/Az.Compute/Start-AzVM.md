---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Start-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Start-AzVM.md
ms.openlocfilehash: e343b9e16f793a760166736edcef6658bde34723
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876001"
---
# <span data-ttu-id="532e7-101">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="532e7-101">Start-AzVM</span></span>

## <span data-ttu-id="532e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="532e7-102">SYNOPSIS</span></span>
<span data-ttu-id="532e7-103">Azure 가상 머신을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="532e7-103">Starts an Azure virtual machine.</span></span>

## <span data-ttu-id="532e7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="532e7-104">SYNTAX</span></span>

### <span data-ttu-id="532e7-105">ResourceGroupNameParameterSetName (기본값)</span><span class="sxs-lookup"><span data-stu-id="532e7-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzVM [-Name] <String> [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="532e7-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="532e7-106">IdParameterSetName</span></span>
```
Start-AzVM [-Name] <String> [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="532e7-107">설명은</span><span class="sxs-lookup"><span data-stu-id="532e7-107">DESCRIPTION</span></span>
<span data-ttu-id="532e7-108">**AzVM** Cmdlet은 Azure 가상 머신을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="532e7-108">The **Start-AzVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="532e7-109">예제의</span><span class="sxs-lookup"><span data-stu-id="532e7-109">EXAMPLES</span></span>

### <span data-ttu-id="532e7-110">예제 1: 가상 컴퓨터 시작</span><span class="sxs-lookup"><span data-stu-id="532e7-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="532e7-111">이 명령은 ResourceGroup11에서 VirtualMachine07 이라는 가상 컴퓨터를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="532e7-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="532e7-112">변수</span><span class="sxs-lookup"><span data-stu-id="532e7-112">PARAMETERS</span></span>

### <span data-ttu-id="532e7-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="532e7-113">-AsJob</span></span>
<span data-ttu-id="532e7-114">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="532e7-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="532e7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="532e7-115">-DefaultProfile</span></span>
<span data-ttu-id="532e7-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="532e7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="532e7-117">-Id</span><span class="sxs-lookup"><span data-stu-id="532e7-117">-Id</span></span>
<span data-ttu-id="532e7-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="532e7-118">The resource group name.</span></span>

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

### <span data-ttu-id="532e7-119">-이름</span><span class="sxs-lookup"><span data-stu-id="532e7-119">-Name</span></span>
<span data-ttu-id="532e7-120">가상 컴퓨터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="532e7-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="532e7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="532e7-121">-ResourceGroupName</span></span>
<span data-ttu-id="532e7-122">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="532e7-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="532e7-123">-확인</span><span class="sxs-lookup"><span data-stu-id="532e7-123">-Confirm</span></span>
<span data-ttu-id="532e7-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="532e7-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="532e7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="532e7-125">-WhatIf</span></span>
<span data-ttu-id="532e7-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="532e7-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="532e7-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="532e7-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="532e7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="532e7-128">CommonParameters</span></span>
<span data-ttu-id="532e7-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="532e7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="532e7-130">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="532e7-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="532e7-131">입력</span><span class="sxs-lookup"><span data-stu-id="532e7-131">INPUTS</span></span>

### <span data-ttu-id="532e7-132">않아야</span><span class="sxs-lookup"><span data-stu-id="532e7-132">None</span></span>
<span data-ttu-id="532e7-133">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="532e7-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="532e7-134">출력</span><span class="sxs-lookup"><span data-stu-id="532e7-134">OUTPUTS</span></span>

### <span data-ttu-id="532e7-135">PSComputeLongRunningOperation를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="532e7-135">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="532e7-136">상속자</span><span class="sxs-lookup"><span data-stu-id="532e7-136">NOTES</span></span>

## <span data-ttu-id="532e7-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="532e7-137">RELATED LINKS</span></span>

[<span data-ttu-id="532e7-138">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="532e7-138">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="532e7-139">새로운 AzVM</span><span class="sxs-lookup"><span data-stu-id="532e7-139">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="532e7-140">제거-AzVM</span><span class="sxs-lookup"><span data-stu-id="532e7-140">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="532e7-141">다시 시작-AzVM</span><span class="sxs-lookup"><span data-stu-id="532e7-141">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="532e7-142">중지-AzVM</span><span class="sxs-lookup"><span data-stu-id="532e7-142">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="532e7-143">업데이트-AzVM</span><span class="sxs-lookup"><span data-stu-id="532e7-143">Update-AzVM</span></span>](./Update-AzVM.md)


