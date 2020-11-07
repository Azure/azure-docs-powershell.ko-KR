---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9A6F140C-9F1C-4701-9603-FC6107FCAF92
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmbootdiagnostics
schema: 2.0.0
ms.openlocfilehash: 2faa28fc0f0e4c27e384c178b96b8d38cae16a3d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882274"
---
# <span data-ttu-id="ccd75-101">Set-AzureRmVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="ccd75-101">Set-AzureRmVMBootDiagnostics</span></span>

## <span data-ttu-id="ccd75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ccd75-102">SYNOPSIS</span></span>
<span data-ttu-id="ccd75-103">가상 컴퓨터의 부팅 진단 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd75-103">Modifies boot diagnostics properties of a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ccd75-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ccd75-104">SYNTAX</span></span>

### <span data-ttu-id="ccd75-105">EnableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="ccd75-105">EnableBootDiagnostics</span></span>
```
Set-AzureRmVMBootDiagnostics [-VM] <PSVirtualMachine> [-Enable] [-ResourceGroupName] <String>
 [[-StorageAccountName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ccd75-106">DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="ccd75-106">DisableBootDiagnostics</span></span>
```
Set-AzureRmVMBootDiagnostics [-VM] <PSVirtualMachine> [-Disable] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ccd75-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ccd75-107">DESCRIPTION</span></span>
<span data-ttu-id="ccd75-108">**AzureRmVMBootDiagnostics** cmdlet은 가상 컴퓨터의 부팅 진단 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd75-108">The **Set-AzureRmVMBootDiagnostics** cmdlet modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="ccd75-109">예제의</span><span class="sxs-lookup"><span data-stu-id="ccd75-109">EXAMPLES</span></span>

### <span data-ttu-id="ccd75-110">예제 1: 부팅 진단 사용</span><span class="sxs-lookup"><span data-stu-id="ccd75-110">Example 1: Enable boot diagnostics</span></span>
```
PS C:\> $VM = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07"
PS C:\> Set-AzureRmVMBootDiagnostics -VM $VM -Enable -ResourceGroupName "ResourceGroup11" -StorageAccountName "DiagnosticStorage"
```

<span data-ttu-id="ccd75-111">첫 번째 명령은 **Get-AzureRmVM** 를 사용 하 여 ContosoVM07 이라는 가상 컴퓨터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ccd75-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzureRmVM**.</span></span>
<span data-ttu-id="ccd75-112">명령이 $VM 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd75-112">The command stores it in the $VM variable.</span></span>

<span data-ttu-id="ccd75-113">두 번째 명령은 $VM에서 가상 컴퓨터에 대 한 부팅 진단을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd75-113">The second command enables boot diagnostics for the virtual machine in $VM.</span></span>
<span data-ttu-id="ccd75-114">진단 데이터는 지정 된 계정에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ccd75-114">Diagnostics data is stored in the specified account.</span></span>

## <span data-ttu-id="ccd75-115">변수</span><span class="sxs-lookup"><span data-stu-id="ccd75-115">PARAMETERS</span></span>

### <span data-ttu-id="ccd75-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccd75-116">-DefaultProfile</span></span>
<span data-ttu-id="ccd75-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ccd75-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ccd75-118">-Disable</span><span class="sxs-lookup"><span data-stu-id="ccd75-118">-Disable</span></span>
<span data-ttu-id="ccd75-119">이 cmdlet이 가상 컴퓨터에 대 한 부팅 진단을 사용 하지 않도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd75-119">Indicates that this cmdlet disables the boot diagnostics for the virtual machine.</span></span>

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

### <span data-ttu-id="ccd75-120">-사용</span><span class="sxs-lookup"><span data-stu-id="ccd75-120">-Enable</span></span>
<span data-ttu-id="ccd75-121">이 cmdlet이 가상 컴퓨터에 대 한 부팅 진단을 사용할 수 있도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd75-121">Indicates that this cmdlet enables the boot diagnostics for the virtual machine.</span></span>

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

### <span data-ttu-id="ccd75-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccd75-122">-ResourceGroupName</span></span>
<span data-ttu-id="ccd75-123">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd75-123">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="ccd75-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ccd75-124">-StorageAccountName</span></span>
<span data-ttu-id="ccd75-125">부팅 진단 데이터를 저장할 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd75-125">Specifies the name of the storage account in which to save boot diagnostics data.</span></span>

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

### <span data-ttu-id="ccd75-126">-VM</span><span class="sxs-lookup"><span data-stu-id="ccd75-126">-VM</span></span>
<span data-ttu-id="ccd75-127">이 cmdlet이 부팅 진단을 변경 하는 가상 컴퓨터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd75-127">Specifies the virtual machine for which this cmdlet changes boot diagnostics.</span></span>
<span data-ttu-id="ccd75-128">가상 컴퓨터 개체를 가져오려면 Get-AzureRmVM cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd75-128">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="ccd75-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccd75-129">CommonParameters</span></span>
<span data-ttu-id="ccd75-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd75-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccd75-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccd75-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccd75-132">입력</span><span class="sxs-lookup"><span data-stu-id="ccd75-132">INPUTS</span></span>

### <span data-ttu-id="ccd75-133">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ccd75-133">PSVirtualMachine</span></span>
<span data-ttu-id="ccd75-134">' VM ' 매개 변수는 파이프라인에서 ' PSVirtualMachine ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd75-134">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="ccd75-135">출력</span><span class="sxs-lookup"><span data-stu-id="ccd75-135">OUTPUTS</span></span>

### <span data-ttu-id="ccd75-136">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd75-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="ccd75-137">상속자</span><span class="sxs-lookup"><span data-stu-id="ccd75-137">NOTES</span></span>

## <span data-ttu-id="ccd75-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ccd75-138">RELATED LINKS</span></span>

[<span data-ttu-id="ccd75-139">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ccd75-139">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="ccd75-140">Get-AzureRmVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="ccd75-140">Get-AzureRmVMBootDiagnosticsData</span></span>](./Get-AzureRmVMBootDiagnosticsData.md)


