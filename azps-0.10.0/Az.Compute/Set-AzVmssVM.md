---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 70AA9747-232E-40F2-845C-35A779F51CD2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmssVM.md
ms.openlocfilehash: 8dde17b43de9db13f1f61c909ee8c88b95761751
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876006"
---
# <span data-ttu-id="9fbbf-101">Set-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="9fbbf-101">Set-AzVmssVM</span></span>

## <span data-ttu-id="9fbbf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9fbbf-102">SYNOPSIS</span></span>
<span data-ttu-id="9fbbf-103">VMSS 인스턴스의 상태를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fbbf-103">Modifies the state of a VMSS instance.</span></span>

## <span data-ttu-id="9fbbf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9fbbf-104">SYNTAX</span></span>

### <span data-ttu-id="9fbbf-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="9fbbf-105">DefaultParameter (Default)</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fbbf-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="9fbbf-106">FriendMethod</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-ReimageAll]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fbbf-107">설명은</span><span class="sxs-lookup"><span data-stu-id="9fbbf-107">DESCRIPTION</span></span>
<span data-ttu-id="9fbbf-108">**AzVmssVM** CMDLET은 Vmss (가상 컴퓨터 크기 집합) 인스턴스의 상태를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fbbf-108">The **Set-AzVmssVM** cmdlet modifies the state of a Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="9fbbf-109">예제의</span><span class="sxs-lookup"><span data-stu-id="9fbbf-109">EXAMPLES</span></span>

## <span data-ttu-id="9fbbf-110">변수</span><span class="sxs-lookup"><span data-stu-id="9fbbf-110">PARAMETERS</span></span>

### <span data-ttu-id="9fbbf-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9fbbf-111">-AsJob</span></span>
<span data-ttu-id="9fbbf-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="9fbbf-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9fbbf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fbbf-113">-DefaultProfile</span></span>
<span data-ttu-id="9fbbf-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9fbbf-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9fbbf-115">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="9fbbf-115">-InstanceId</span></span>
<span data-ttu-id="9fbbf-116">이 cmdlet에서 상태를 수정 하는 VMSS 인스턴스의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fbbf-116">Specifies the ID of the VMSS instance for which this cmdlet modifies state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fbbf-117">-이미지로</span><span class="sxs-lookup"><span data-stu-id="9fbbf-117">-Reimage</span></span>
<span data-ttu-id="9fbbf-118">이 cmdlet이 VMSS 인스턴스를 다시 이미지로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fbbf-118">Indicates that this cmdlet reimages the VMSS instance.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fbbf-119">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="9fbbf-119">-ReimageAll</span></span>
<span data-ttu-id="9fbbf-120">Cmdlet이 VMSS 인스턴스의 모든 디스크를 다시 이미지로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fbbf-120">Indicates that the cmdlet reimages all the disks in the VMSS instance.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fbbf-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fbbf-121">-ResourceGroupName</span></span>
<span data-ttu-id="9fbbf-122">VMSS 인스턴스가 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fbbf-122">Specifies the name of the resource group that contains the VMSS instance.</span></span>

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

### <span data-ttu-id="9fbbf-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="9fbbf-123">-VMScaleSetName</span></span>
<span data-ttu-id="9fbbf-124">이 cmdlet이 수정 하는 VMSS 인스턴스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fbbf-124">Specifies the name of the VMSS instance that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="9fbbf-125">-확인</span><span class="sxs-lookup"><span data-stu-id="9fbbf-125">-Confirm</span></span>
<span data-ttu-id="9fbbf-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fbbf-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fbbf-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fbbf-127">-WhatIf</span></span>
<span data-ttu-id="9fbbf-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9fbbf-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9fbbf-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9fbbf-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fbbf-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fbbf-130">CommonParameters</span></span>
<span data-ttu-id="9fbbf-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fbbf-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fbbf-132">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fbbf-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fbbf-133">입력</span><span class="sxs-lookup"><span data-stu-id="9fbbf-133">INPUTS</span></span>

### <span data-ttu-id="9fbbf-134">않아야</span><span class="sxs-lookup"><span data-stu-id="9fbbf-134">None</span></span>
<span data-ttu-id="9fbbf-135">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9fbbf-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9fbbf-136">출력</span><span class="sxs-lookup"><span data-stu-id="9fbbf-136">OUTPUTS</span></span>

### <span data-ttu-id="9fbbf-137">PSOperationStatusResponse의. m a.</span><span class="sxs-lookup"><span data-stu-id="9fbbf-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="9fbbf-138">상속자</span><span class="sxs-lookup"><span data-stu-id="9fbbf-138">NOTES</span></span>

## <span data-ttu-id="9fbbf-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9fbbf-139">RELATED LINKS</span></span>

[<span data-ttu-id="9fbbf-140">Get-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="9fbbf-140">Get-AzVmssVM</span></span>](./Get-AzVmssVM.md)
