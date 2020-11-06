---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 70AA9747-232E-40F2-845C-35A779F51CD2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssVM.md
ms.openlocfilehash: d035844046e238694cfec72feda9eab61b7714d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531082"
---
# <span data-ttu-id="57ef0-101">Set-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="57ef0-101">Set-AzureRmVmssVM</span></span>

## <span data-ttu-id="57ef0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57ef0-102">SYNOPSIS</span></span>
<span data-ttu-id="57ef0-103">VMSS 인스턴스의 상태를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57ef0-103">Modifies the state of a VMSS instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57ef0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="57ef0-104">SYNTAX</span></span>

### <span data-ttu-id="57ef0-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="57ef0-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Reimage]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57ef0-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="57ef0-106">FriendMethod</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-ReimageAll]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57ef0-107">설명은</span><span class="sxs-lookup"><span data-stu-id="57ef0-107">DESCRIPTION</span></span>
<span data-ttu-id="57ef0-108">**AzureRmVmssVM** CMDLET은 Vmss (가상 컴퓨터 크기 집합) 인스턴스의 상태를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57ef0-108">The **Set-AzureRmVmssVM** cmdlet modifies the state of a Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="57ef0-109">예제의</span><span class="sxs-lookup"><span data-stu-id="57ef0-109">EXAMPLES</span></span>

## <span data-ttu-id="57ef0-110">변수</span><span class="sxs-lookup"><span data-stu-id="57ef0-110">PARAMETERS</span></span>

### <span data-ttu-id="57ef0-111">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="57ef0-111">-InstanceId</span></span>
<span data-ttu-id="57ef0-112">이 cmdlet에서 상태를 수정 하는 VMSS 인스턴스의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57ef0-112">Specifies the ID of the VMSS instance for which this cmdlet modifies state.</span></span>

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

### <span data-ttu-id="57ef0-113">-이미지로</span><span class="sxs-lookup"><span data-stu-id="57ef0-113">-Reimage</span></span>
<span data-ttu-id="57ef0-114">이 cmdlet이 VMSS 인스턴스를 다시 이미지로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="57ef0-114">Indicates that this cmdlet reimages the VMSS instance.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57ef0-115">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="57ef0-115">-ReimageAll</span></span>
<span data-ttu-id="57ef0-116">Cmdlet이 VMSS 인스턴스의 모든 디스크를 다시 이미지로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="57ef0-116">Indicates that the cmdlet reimages all the disks in the VMSS instance.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57ef0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57ef0-117">-ResourceGroupName</span></span>
<span data-ttu-id="57ef0-118">VMSS 인스턴스가 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57ef0-118">Specifies the name of the resource group that contains the VMSS instance.</span></span>

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

### <span data-ttu-id="57ef0-119">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="57ef0-119">-VMScaleSetName</span></span>
<span data-ttu-id="57ef0-120">이 cmdlet이 수정 하는 VMSS 인스턴스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57ef0-120">Specifies the name of the VMSS instance that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="57ef0-121">-확인</span><span class="sxs-lookup"><span data-stu-id="57ef0-121">-Confirm</span></span>
<span data-ttu-id="57ef0-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="57ef0-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57ef0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57ef0-123">-WhatIf</span></span>
<span data-ttu-id="57ef0-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="57ef0-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="57ef0-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="57ef0-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57ef0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57ef0-126">CommonParameters</span></span>
<span data-ttu-id="57ef0-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="57ef0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57ef0-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57ef0-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57ef0-129">입력</span><span class="sxs-lookup"><span data-stu-id="57ef0-129">INPUTS</span></span>

### <span data-ttu-id="57ef0-130">않아야</span><span class="sxs-lookup"><span data-stu-id="57ef0-130">None</span></span>
<span data-ttu-id="57ef0-131">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="57ef0-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="57ef0-132">출력</span><span class="sxs-lookup"><span data-stu-id="57ef0-132">OUTPUTS</span></span>

## <span data-ttu-id="57ef0-133">상속자</span><span class="sxs-lookup"><span data-stu-id="57ef0-133">NOTES</span></span>

## <span data-ttu-id="57ef0-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="57ef0-134">RELATED LINKS</span></span>

[<span data-ttu-id="57ef0-135">Get-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="57ef0-135">Get-AzureRmVmssVM</span></span>](./Get-AzureRmVmssVM.md)
