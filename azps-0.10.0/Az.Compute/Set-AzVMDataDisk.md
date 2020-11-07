---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: C453485D-67A7-480E-83F6-527D4F5EBC93
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMDataDisk.md
ms.openlocfilehash: b927e9b61e4d76795e35f2356b900b959a94e082
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876873"
---
# <span data-ttu-id="3a19c-101">Set-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="3a19c-101">Set-AzVMDataDisk</span></span>

## <span data-ttu-id="3a19c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a19c-102">SYNOPSIS</span></span>
<span data-ttu-id="3a19c-103">가상 컴퓨터 데이터 디스크의 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a19c-103">Modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="3a19c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3a19c-104">SYNTAX</span></span>

### <span data-ttu-id="3a19c-105">ChangeWithName</span><span class="sxs-lookup"><span data-stu-id="3a19c-105">ChangeWithName</span></span>
```
Set-AzVMDataDisk [-VM] <PSVirtualMachine> [-Name] <String> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <StorageAccountTypes>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a19c-106">ChangeWithLun</span><span class="sxs-lookup"><span data-stu-id="3a19c-106">ChangeWithLun</span></span>
```
Set-AzVMDataDisk [-VM] <PSVirtualMachine> [-Lun] <Int32> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <StorageAccountTypes>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a19c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="3a19c-107">DESCRIPTION</span></span>
<span data-ttu-id="3a19c-108">**AzVMDataDisk** cmdlet은 가상 컴퓨터 데이터 디스크의 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a19c-108">The **Set-AzVMDataDisk** cmdlet modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="3a19c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="3a19c-109">EXAMPLES</span></span>

### <span data-ttu-id="3a19c-110">예제 1: 데이터 디스크의 캐싱 모드 수정</span><span class="sxs-lookup"><span data-stu-id="3a19c-110">Example 1: Modify the caching mode of a data disk</span></span>
```
PS C:\> $VM = Get-AzVM -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
PS C:\> Set-AzVMDataDisk -VM $VM -Name "DataDisk01" -Caching ReadWrite | Update-AzVM
```

<span data-ttu-id="3a19c-111">첫 번째 명령은 **Get-AzVM** 를 사용 하 여 ContosoVM07 이라는 가상 컴퓨터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3a19c-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzVM**.</span></span>
<span data-ttu-id="3a19c-112">명령이 $VM 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a19c-112">The command stores it in the $VM variable.</span></span>

<span data-ttu-id="3a19c-113">두 번째 명령은 $VM의 가상 컴퓨터에서 DataDisk01 이라는 데이터 디스크에 대 한 캐싱 모드를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a19c-113">The second command modifies the caching mode for the data disk named DataDisk01 on the virtual machine in $VM.</span></span>
<span data-ttu-id="3a19c-114">이 명령은 결과를 변경 내용을 구현 하는 Update-AzVM cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a19c-114">The command passes the result to the Update-AzVM cmdlet, which implements your changes.</span></span>
<span data-ttu-id="3a19c-115">Cashing mode를 변경 하면 가상 컴퓨터가 다시 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3a19c-115">A change to the cashing mode causes the virtual machine to restart.</span></span>

## <span data-ttu-id="3a19c-116">변수</span><span class="sxs-lookup"><span data-stu-id="3a19c-116">PARAMETERS</span></span>

### <span data-ttu-id="3a19c-117">-캐싱</span><span class="sxs-lookup"><span data-stu-id="3a19c-117">-Caching</span></span>
<span data-ttu-id="3a19c-118">디스크의 캐싱 모드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a19c-118">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="3a19c-119">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="3a19c-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3a19c-120">읽기</span><span class="sxs-lookup"><span data-stu-id="3a19c-120">ReadOnly</span></span>
- <span data-ttu-id="3a19c-121">쓰기</span><span class="sxs-lookup"><span data-stu-id="3a19c-121">ReadWrite</span></span>

<span data-ttu-id="3a19c-122">기본값은 ReadWrite입니다.</span><span class="sxs-lookup"><span data-stu-id="3a19c-122">The default value is ReadWrite.</span></span>
<span data-ttu-id="3a19c-123">이 값을 변경 하면 가상 컴퓨터가 다시 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3a19c-123">Changing this value causes the virtual machine to restart.</span></span>

<span data-ttu-id="3a19c-124">이 설정은 디스크의 일관성 및 성능에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3a19c-124">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="3a19c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a19c-125">-DefaultProfile</span></span>
<span data-ttu-id="3a19c-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3a19c-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a19c-127">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="3a19c-127">-DiskSizeInGB</span></span>
<span data-ttu-id="3a19c-128">데이터 디스크의 크기 (기가바이트)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a19c-128">Specifies the size, in gigabytes, for the data disk.</span></span>

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

### <span data-ttu-id="3a19c-129">-Lun</span><span class="sxs-lookup"><span data-stu-id="3a19c-129">-Lun</span></span>
<span data-ttu-id="3a19c-130">이 cmdlet이 수정 하는 데이터 디스크의 LUN (논리 단위 번호)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a19c-130">Specifies the logical unit number (LUN) of the data disk that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="3a19c-131">-이름</span><span class="sxs-lookup"><span data-stu-id="3a19c-131">-Name</span></span>
<span data-ttu-id="3a19c-132">이 cmdlet이 수정 하는 데이터 디스크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a19c-132">Specifies the name of the data disk that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="3a19c-133">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="3a19c-133">-StorageAccountType</span></span>
<span data-ttu-id="3a19c-134">가상 컴퓨터 관리 디스크의 계정 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="3a19c-134">The virtual machine managed disk's account type.</span></span>

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

### <span data-ttu-id="3a19c-135">-VM</span><span class="sxs-lookup"><span data-stu-id="3a19c-135">-VM</span></span>
<span data-ttu-id="3a19c-136">이 cmdlet이 데이터 디스크를 수정할 가상 컴퓨터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a19c-136">Specifies the virtual machine for which this cmdlet modifies a data disk.</span></span>
<span data-ttu-id="3a19c-137">가상 컴퓨터 개체를 가져오려면 Get-AzVM cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a19c-137">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="3a19c-138">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="3a19c-138">-WriteAccelerator</span></span>
<span data-ttu-id="3a19c-139">데이터 디스크에서 WriteAccelerator를 사용할지 아니면 disabled를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a19c-139">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

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

### <span data-ttu-id="3a19c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a19c-140">CommonParameters</span></span>
<span data-ttu-id="3a19c-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a19c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a19c-142">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a19c-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a19c-143">입력</span><span class="sxs-lookup"><span data-stu-id="3a19c-143">INPUTS</span></span>

### <span data-ttu-id="3a19c-144">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="3a19c-144">PSVirtualMachine</span></span>
<span data-ttu-id="3a19c-145">' VM ' 매개 변수는 파이프라인에서 ' PSVirtualMachine ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a19c-145">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="3a19c-146">출력</span><span class="sxs-lookup"><span data-stu-id="3a19c-146">OUTPUTS</span></span>

### <span data-ttu-id="3a19c-147">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a19c-147">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="3a19c-148">상속자</span><span class="sxs-lookup"><span data-stu-id="3a19c-148">NOTES</span></span>

## <span data-ttu-id="3a19c-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3a19c-149">RELATED LINKS</span></span>

[<span data-ttu-id="3a19c-150">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="3a19c-150">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="3a19c-151">업데이트-AzVM</span><span class="sxs-lookup"><span data-stu-id="3a19c-151">Update-AzVM</span></span>](./Update-AzVM.md)


