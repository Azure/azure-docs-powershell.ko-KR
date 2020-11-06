---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 9A6F140C-9F1C-4701-9603-FC6107FCAF92
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMBootDiagnostics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMBootDiagnostics.md
ms.openlocfilehash: c02551e09fa0a5ce484883a4b2925c0c172e537f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529012"
---
# <span data-ttu-id="418d2-101">Set-AzureRmVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="418d2-101">Set-AzureRmVMBootDiagnostics</span></span>

## <span data-ttu-id="418d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="418d2-102">SYNOPSIS</span></span>
<span data-ttu-id="418d2-103">가상 컴퓨터의 부팅 진단 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="418d2-103">Modifies boot diagnostics properties of a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="418d2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="418d2-104">SYNTAX</span></span>

### <span data-ttu-id="418d2-105">EnableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="418d2-105">EnableBootDiagnostics</span></span>
```
Set-AzureRmVMBootDiagnostics [-VM] <PSVirtualMachine> [-Enable] [-ResourceGroupName] <String>
 [[-StorageAccountName] <String>] [<CommonParameters>]
```

### <span data-ttu-id="418d2-106">DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="418d2-106">DisableBootDiagnostics</span></span>
```
Set-AzureRmVMBootDiagnostics [-VM] <PSVirtualMachine> [-Disable] [<CommonParameters>]
```

## <span data-ttu-id="418d2-107">설명은</span><span class="sxs-lookup"><span data-stu-id="418d2-107">DESCRIPTION</span></span>
<span data-ttu-id="418d2-108">**AzureRmVMBootDiagnostics** cmdlet은 가상 컴퓨터의 부팅 진단 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="418d2-108">The **Set-AzureRmVMBootDiagnostics** cmdlet modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="418d2-109">예제의</span><span class="sxs-lookup"><span data-stu-id="418d2-109">EXAMPLES</span></span>

### <span data-ttu-id="418d2-110">예제 1: 부팅 진단 사용</span><span class="sxs-lookup"><span data-stu-id="418d2-110">Example 1: Enable boot diagnostics</span></span>
```
PS C:\> $VM = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07"
PS C:\> Set-AzureRmVMBootDiagnostics -VM $VM -Enable -ResourceGroupName "ResourceGroup11" -StorageAccountName "DiagnosticStorage"
PS C:\> Update-AzureRmVM -ResourceGroup "ResourceGroup11" -VM $VM
```

<span data-ttu-id="418d2-111">첫 번째 명령은 **Get-AzureRmVM** 를 사용 하 여 ContosoVM07 이라는 가상 컴퓨터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="418d2-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzureRmVM**.</span></span>
<span data-ttu-id="418d2-112">명령이 $VM 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="418d2-112">The command stores it in the $VM variable.</span></span>

<span data-ttu-id="418d2-113">두 번째 명령은 $VM에서 가상 컴퓨터에 대 한 부팅 진단을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="418d2-113">The second command enables boot diagnostics for the virtual machine in $VM.</span></span>
<span data-ttu-id="418d2-114">진단 데이터는 지정 된 계정에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="418d2-114">Diagnostics data is stored in the specified account.</span></span>

## <span data-ttu-id="418d2-115">변수</span><span class="sxs-lookup"><span data-stu-id="418d2-115">PARAMETERS</span></span>

### <span data-ttu-id="418d2-116">-Disable</span><span class="sxs-lookup"><span data-stu-id="418d2-116">-Disable</span></span>
<span data-ttu-id="418d2-117">이 cmdlet이 가상 컴퓨터에 대 한 부팅 진단을 사용 하지 않도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="418d2-117">Indicates that this cmdlet disables the boot diagnostics for the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableBootDiagnostics
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="418d2-118">-사용</span><span class="sxs-lookup"><span data-stu-id="418d2-118">-Enable</span></span>
<span data-ttu-id="418d2-119">이 cmdlet이 가상 컴퓨터에 대 한 부팅 진단을 사용할 수 있도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="418d2-119">Indicates that this cmdlet enables the boot diagnostics for the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnableBootDiagnostics
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="418d2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="418d2-120">-ResourceGroupName</span></span>
<span data-ttu-id="418d2-121">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="418d2-121">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: EnableBootDiagnostics
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="418d2-122">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="418d2-122">-StorageAccountName</span></span>
<span data-ttu-id="418d2-123">부팅 진단 데이터를 저장할 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="418d2-123">Specifies the name of the storage account in which to save boot diagnostics data.</span></span>

```yaml
Type: String
Parameter Sets: EnableBootDiagnostics
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="418d2-124">-VM</span><span class="sxs-lookup"><span data-stu-id="418d2-124">-VM</span></span>
<span data-ttu-id="418d2-125">이 cmdlet이 부팅 진단을 변경 하는 가상 컴퓨터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="418d2-125">Specifies the virtual machine for which this cmdlet changes boot diagnostics.</span></span>
<span data-ttu-id="418d2-126">가상 컴퓨터 개체를 가져오려면 Get-AzureRmVM cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="418d2-126">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="418d2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="418d2-127">CommonParameters</span></span>
<span data-ttu-id="418d2-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="418d2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="418d2-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="418d2-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="418d2-130">입력</span><span class="sxs-lookup"><span data-stu-id="418d2-130">INPUTS</span></span>

### <span data-ttu-id="418d2-131">않아야</span><span class="sxs-lookup"><span data-stu-id="418d2-131">None</span></span>
<span data-ttu-id="418d2-132">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="418d2-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="418d2-133">출력</span><span class="sxs-lookup"><span data-stu-id="418d2-133">OUTPUTS</span></span>

## <span data-ttu-id="418d2-134">상속자</span><span class="sxs-lookup"><span data-stu-id="418d2-134">NOTES</span></span>

## <span data-ttu-id="418d2-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="418d2-135">RELATED LINKS</span></span>

[<span data-ttu-id="418d2-136">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="418d2-136">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="418d2-137">Get-AzureRmVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="418d2-137">Get-AzureRmVMBootDiagnosticsData</span></span>](./Get-AzureRmVMBootDiagnosticsData.md)


