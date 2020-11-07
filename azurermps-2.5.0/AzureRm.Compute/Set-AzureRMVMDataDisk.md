---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: C453485D-67A7-480E-83F6-527D4F5EBC93
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmdatadisk
schema: 2.0.0
ms.openlocfilehash: 53ad88f6e3df11eb3a8f2f9c4b21af40b9ea614b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93883133"
---
# <span data-ttu-id="8366e-101">Set-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="8366e-101">Set-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="8366e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8366e-102">SYNOPSIS</span></span>
<span data-ttu-id="8366e-103">가상 컴퓨터 데이터 디스크의 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8366e-103">Modifies properties of a virtual machine data disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8366e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8366e-104">SYNTAX</span></span>

### <span data-ttu-id="8366e-105">ChangeWithName</span><span class="sxs-lookup"><span data-stu-id="8366e-105">ChangeWithName</span></span>
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Name] <String> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <StorageAccountTypes>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8366e-106">ChangeWithLun</span><span class="sxs-lookup"><span data-stu-id="8366e-106">ChangeWithLun</span></span>
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Lun] <Int32> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <StorageAccountTypes>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8366e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="8366e-107">DESCRIPTION</span></span>
<span data-ttu-id="8366e-108">**AzureRmVMDataDisk** cmdlet은 가상 컴퓨터 데이터 디스크의 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8366e-108">The **Set-AzureRmVMDataDisk** cmdlet modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="8366e-109">예제의</span><span class="sxs-lookup"><span data-stu-id="8366e-109">EXAMPLES</span></span>

### <span data-ttu-id="8366e-110">예제 1: 데이터 디스크의 캐싱 모드 수정</span><span class="sxs-lookup"><span data-stu-id="8366e-110">Example 1: Modify the caching mode of a data disk</span></span>
```
PS C:\> $VM = Get-AzureRMVM -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
PS C:\> Set-AzureRmVMDataDisk -VM $VM -Name "DataDisk01" -Caching ReadWrite | Update-AzureRmVM
```

<span data-ttu-id="8366e-111">첫 번째 명령은 **Get-AzureRmVM** 를 사용 하 여 ContosoVM07 이라는 가상 컴퓨터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8366e-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzureRmVM**.</span></span>
<span data-ttu-id="8366e-112">명령이 $VM 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8366e-112">The command stores it in the $VM variable.</span></span>

<span data-ttu-id="8366e-113">두 번째 명령은 $VM의 가상 컴퓨터에서 DataDisk01 이라는 데이터 디스크에 대 한 캐싱 모드를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8366e-113">The second command modifies the caching mode for the data disk named DataDisk01 on the virtual machine in $VM.</span></span>
<span data-ttu-id="8366e-114">이 명령은 결과를 변경 내용을 구현 하는 Update-AzureRmVM cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="8366e-114">The command passes the result to the Update-AzureRmVM cmdlet, which implements your changes.</span></span>
<span data-ttu-id="8366e-115">Cashing mode를 변경 하면 가상 컴퓨터가 다시 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8366e-115">A change to the cashing mode causes the virtual machine to restart.</span></span>

## <span data-ttu-id="8366e-116">변수</span><span class="sxs-lookup"><span data-stu-id="8366e-116">PARAMETERS</span></span>

### <span data-ttu-id="8366e-117">-캐싱</span><span class="sxs-lookup"><span data-stu-id="8366e-117">-Caching</span></span>
<span data-ttu-id="8366e-118">디스크의 캐싱 모드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8366e-118">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="8366e-119">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="8366e-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8366e-120">읽기</span><span class="sxs-lookup"><span data-stu-id="8366e-120">ReadOnly</span></span>
- <span data-ttu-id="8366e-121">쓰기</span><span class="sxs-lookup"><span data-stu-id="8366e-121">ReadWrite</span></span>

<span data-ttu-id="8366e-122">기본값은 ReadWrite입니다.</span><span class="sxs-lookup"><span data-stu-id="8366e-122">The default value is ReadWrite.</span></span>
<span data-ttu-id="8366e-123">이 값을 변경 하면 가상 컴퓨터가 다시 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8366e-123">Changing this value causes the virtual machine to restart.</span></span>

<span data-ttu-id="8366e-124">이 설정은 디스크의 일관성 및 성능에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8366e-124">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8366e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8366e-125">-DefaultProfile</span></span>
<span data-ttu-id="8366e-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8366e-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8366e-127">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="8366e-127">-DiskSizeInGB</span></span>
<span data-ttu-id="8366e-128">데이터 디스크의 크기 (기가바이트)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8366e-128">Specifies the size, in gigabytes, for the data disk.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8366e-129">-Lun</span><span class="sxs-lookup"><span data-stu-id="8366e-129">-Lun</span></span>
<span data-ttu-id="8366e-130">이 cmdlet이 수정 하는 데이터 디스크의 LUN (논리 단위 번호)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8366e-130">Specifies the logical unit number (LUN) of the data disk that this cmdlet modifies.</span></span>

```yaml
Type: Int32
Parameter Sets: ChangeWithLun
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8366e-131">-이름</span><span class="sxs-lookup"><span data-stu-id="8366e-131">-Name</span></span>
<span data-ttu-id="8366e-132">이 cmdlet이 수정 하는 데이터 디스크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8366e-132">Specifies the name of the data disk that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: ChangeWithName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8366e-133">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="8366e-133">-StorageAccountType</span></span>
<span data-ttu-id="8366e-134">가상 컴퓨터 관리 디스크의 계정 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="8366e-134">The virtual machine managed disk's account type.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8366e-135">-VM</span><span class="sxs-lookup"><span data-stu-id="8366e-135">-VM</span></span>
<span data-ttu-id="8366e-136">이 cmdlet이 데이터 디스크를 수정할 가상 컴퓨터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8366e-136">Specifies the virtual machine for which this cmdlet modifies a data disk.</span></span>
<span data-ttu-id="8366e-137">가상 컴퓨터 개체를 가져오려면 Get-AzureRmVM cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8366e-137">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="8366e-138">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="8366e-138">-WriteAccelerator</span></span>
<span data-ttu-id="8366e-139">데이터 디스크에서 WriteAccelerator를 사용할지 아니면 disabled를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8366e-139">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

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

### <span data-ttu-id="8366e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8366e-140">CommonParameters</span></span>
<span data-ttu-id="8366e-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8366e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8366e-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8366e-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8366e-143">입력</span><span class="sxs-lookup"><span data-stu-id="8366e-143">INPUTS</span></span>

### <span data-ttu-id="8366e-144">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="8366e-144">PSVirtualMachine</span></span>
<span data-ttu-id="8366e-145">' VM ' 매개 변수는 파이프라인에서 ' PSVirtualMachine ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8366e-145">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="8366e-146">출력</span><span class="sxs-lookup"><span data-stu-id="8366e-146">OUTPUTS</span></span>

### <span data-ttu-id="8366e-147">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="8366e-147">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="8366e-148">상속자</span><span class="sxs-lookup"><span data-stu-id="8366e-148">NOTES</span></span>

## <span data-ttu-id="8366e-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8366e-149">RELATED LINKS</span></span>

[<span data-ttu-id="8366e-150">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8366e-150">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="8366e-151">업데이트-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8366e-151">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


