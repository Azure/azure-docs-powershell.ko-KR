---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVM.md
ms.openlocfilehash: 32e633d1f9fea877ef81b6c6e7ef5e8bb09da81a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048388"
---
# <span data-ttu-id="e6167-101">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="e6167-101">Start-AzVM</span></span>

## <span data-ttu-id="e6167-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6167-102">SYNOPSIS</span></span>
<span data-ttu-id="e6167-103">Azure 가상 머신을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6167-103">Starts an Azure virtual machine.</span></span>

## <span data-ttu-id="e6167-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e6167-104">SYNTAX</span></span>

### <span data-ttu-id="e6167-105">ResourceGroupNameParameterSetName (기본값)</span><span class="sxs-lookup"><span data-stu-id="e6167-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzVM [-Name] <String> [-NoWait] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6167-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="e6167-106">IdParameterSetName</span></span>
```
Start-AzVM [-NoWait] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e6167-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e6167-107">DESCRIPTION</span></span>
<span data-ttu-id="e6167-108">**AzVM** Cmdlet은 Azure 가상 머신을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6167-108">The **Start-AzVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="e6167-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e6167-109">EXAMPLES</span></span>

### <span data-ttu-id="e6167-110">예제 1: 가상 컴퓨터 시작</span><span class="sxs-lookup"><span data-stu-id="e6167-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="e6167-111">이 명령은 ResourceGroup11에서 VirtualMachine07 이라는 가상 컴퓨터를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6167-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="e6167-112">변수</span><span class="sxs-lookup"><span data-stu-id="e6167-112">PARAMETERS</span></span>

### <span data-ttu-id="e6167-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e6167-113">-AsJob</span></span>
<span data-ttu-id="e6167-114">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6167-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="e6167-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6167-115">-DefaultProfile</span></span>
<span data-ttu-id="e6167-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e6167-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6167-117">-Id</span><span class="sxs-lookup"><span data-stu-id="e6167-117">-Id</span></span>
<span data-ttu-id="e6167-118">가상 컴퓨터의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e6167-118">The ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6167-119">-이름</span><span class="sxs-lookup"><span data-stu-id="e6167-119">-Name</span></span>
<span data-ttu-id="e6167-120">가상 컴퓨터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e6167-120">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6167-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e6167-121">-NoWait</span></span>
<span data-ttu-id="e6167-122">작업이 완료 되기 전에 작업을 시작 하 고 즉시 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6167-122">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="e6167-123">작업이 성공적으로 완료 되었는지 확인 하려면 다른 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6167-123">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="e6167-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6167-124">-ResourceGroupName</span></span>
<span data-ttu-id="e6167-125">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6167-125">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6167-126">-확인</span><span class="sxs-lookup"><span data-stu-id="e6167-126">-Confirm</span></span>
<span data-ttu-id="e6167-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6167-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6167-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6167-128">-WhatIf</span></span>
<span data-ttu-id="e6167-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e6167-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e6167-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e6167-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6167-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6167-131">CommonParameters</span></span>
<span data-ttu-id="e6167-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6167-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6167-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e6167-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6167-134">입력</span><span class="sxs-lookup"><span data-stu-id="e6167-134">INPUTS</span></span>

### <span data-ttu-id="e6167-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e6167-135">System.String</span></span>

## <span data-ttu-id="e6167-136">출력</span><span class="sxs-lookup"><span data-stu-id="e6167-136">OUTPUTS</span></span>

### <span data-ttu-id="e6167-137">PSComputeLongRunningOperation를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6167-137">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="e6167-138">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="e6167-138">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="e6167-139">상속자</span><span class="sxs-lookup"><span data-stu-id="e6167-139">NOTES</span></span>

## <span data-ttu-id="e6167-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e6167-140">RELATED LINKS</span></span>

[<span data-ttu-id="e6167-141">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="e6167-141">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="e6167-142">새로운 AzVM</span><span class="sxs-lookup"><span data-stu-id="e6167-142">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="e6167-143">제거-AzVM</span><span class="sxs-lookup"><span data-stu-id="e6167-143">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="e6167-144">다시 시작-AzVM</span><span class="sxs-lookup"><span data-stu-id="e6167-144">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="e6167-145">중지-AzVM</span><span class="sxs-lookup"><span data-stu-id="e6167-145">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="e6167-146">업데이트-AzVM</span><span class="sxs-lookup"><span data-stu-id="e6167-146">Update-AzVM</span></span>](./Update-AzVM.md)


