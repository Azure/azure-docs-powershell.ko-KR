---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssbootdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssBootDiagnostic.md
ms.openlocfilehash: 31da1c621e8f3dc91c303abd6c70476f40602de4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213082"
---
# <span data-ttu-id="95fd7-101">Set-AzVmssBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="95fd7-101">Set-AzVmssBootDiagnostic</span></span>

## <span data-ttu-id="95fd7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95fd7-102">SYNOPSIS</span></span>
<span data-ttu-id="95fd7-103">가상 컴퓨터 크기 집합 부팅 진단 프로필을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="95fd7-103">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="95fd7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="95fd7-104">SYNTAX</span></span>

```
Set-AzVmssBootDiagnostic [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Enabled] <Boolean>]
 [[-StorageUri] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95fd7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="95fd7-105">DESCRIPTION</span></span>
<span data-ttu-id="95fd7-106">가상 컴퓨터 크기 집합 부팅 진단 프로필을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="95fd7-106">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="95fd7-107">예제의</span><span class="sxs-lookup"><span data-stu-id="95fd7-107">EXAMPLES</span></span>

### <span data-ttu-id="95fd7-108">예제 1: VMSS에 대 한 부팅 진단 프로필 속성 설정</span><span class="sxs-lookup"><span data-stu-id="95fd7-108">Example 1: Set the boot diagnostics profile property for a VMSS</span></span>
```
PS C:\> $vmss = New-AzVmssConfig -Location $loc -SkuCapacity 2 -SkuName 'Standard_A0'
PS C:\> Set-AzVmssBootDiagnostic -VirtualMachineScaleSet $vmss -Enabled $true -StorageUri $storageUri;
PS C:\> New-AzVmss -ResourceGroupName $rgname -Name "ContosoVMSS" -VirtualMachineScaleSet $vmss;
```

<span data-ttu-id="95fd7-109">이 명령은 ContosoVMSS 이라는 VMSS에 대 한 부팅 진단 프로필 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="95fd7-109">This command sets boot diagnostics profile property for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="95fd7-110">변수</span><span class="sxs-lookup"><span data-stu-id="95fd7-110">PARAMETERS</span></span>

### <span data-ttu-id="95fd7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95fd7-111">-DefaultProfile</span></span>
<span data-ttu-id="95fd7-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="95fd7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95fd7-113">-사용</span><span class="sxs-lookup"><span data-stu-id="95fd7-113">-Enabled</span></span>
<span data-ttu-id="95fd7-114">가상 컴퓨터 크기 집합에 부팅 진단을 사용할지 여부</span><span class="sxs-lookup"><span data-stu-id="95fd7-114">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95fd7-115">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="95fd7-115">-StorageUri</span></span>
<span data-ttu-id="95fd7-116">콘솔 출력과 스크린샷을 배치 하는 데 사용할 저장소 계정의 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="95fd7-116">URI of the storage account to use for placing the console output and screenshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95fd7-117">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="95fd7-117">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="95fd7-118">VMSS 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="95fd7-118">Specifies the VMSS object.</span></span>
<span data-ttu-id="95fd7-119">New-AzVmssConfig cmdlet을 사용 하 여 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95fd7-119">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95fd7-120">-확인</span><span class="sxs-lookup"><span data-stu-id="95fd7-120">-Confirm</span></span>
<span data-ttu-id="95fd7-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="95fd7-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95fd7-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95fd7-122">-WhatIf</span></span>
<span data-ttu-id="95fd7-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="95fd7-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95fd7-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="95fd7-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95fd7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95fd7-125">CommonParameters</span></span>
<span data-ttu-id="95fd7-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="95fd7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95fd7-127">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="95fd7-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95fd7-128">입력</span><span class="sxs-lookup"><span data-stu-id="95fd7-128">INPUTS</span></span>

### <span data-ttu-id="95fd7-129">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="95fd7-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="95fd7-130">시스템 Null 허용 ' 1 [[CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="95fd7-130">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="95fd7-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="95fd7-131">System.String</span></span>

## <span data-ttu-id="95fd7-132">출력</span><span class="sxs-lookup"><span data-stu-id="95fd7-132">OUTPUTS</span></span>

### <span data-ttu-id="95fd7-133">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="95fd7-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="95fd7-134">상속자</span><span class="sxs-lookup"><span data-stu-id="95fd7-134">NOTES</span></span>

## <span data-ttu-id="95fd7-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="95fd7-135">RELATED LINKS</span></span>
