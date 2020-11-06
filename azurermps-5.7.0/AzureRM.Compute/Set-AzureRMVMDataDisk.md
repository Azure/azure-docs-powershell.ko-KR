---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: C453485D-67A7-480E-83F6-527D4F5EBC93
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMDataDisk.md
ms.openlocfilehash: 2f961f144bc322cb1b1b12001ed006bc783ed67e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531753"
---
# <span data-ttu-id="fee73-101">Set-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="fee73-101">Set-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="fee73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fee73-102">SYNOPSIS</span></span>
<span data-ttu-id="fee73-103">가상 컴퓨터 데이터 디스크의 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fee73-103">Modifies properties of a virtual machine data disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fee73-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fee73-104">SYNTAX</span></span>

### <span data-ttu-id="fee73-105">ChangeWithName</span><span class="sxs-lookup"><span data-stu-id="fee73-105">ChangeWithName</span></span>
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Name] <String> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="fee73-106">ChangeWithLun</span><span class="sxs-lookup"><span data-stu-id="fee73-106">ChangeWithLun</span></span>
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Lun] <Int32> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="fee73-107">설명은</span><span class="sxs-lookup"><span data-stu-id="fee73-107">DESCRIPTION</span></span>
<span data-ttu-id="fee73-108">**AzureRmVMDataDisk** cmdlet은 가상 컴퓨터 데이터 디스크의 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fee73-108">The **Set-AzureRmVMDataDisk** cmdlet modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="fee73-109">예제의</span><span class="sxs-lookup"><span data-stu-id="fee73-109">EXAMPLES</span></span>

### <span data-ttu-id="fee73-110">예제 1: 데이터 디스크의 캐싱 모드 수정</span><span class="sxs-lookup"><span data-stu-id="fee73-110">Example 1: Modify the caching mode of a data disk</span></span>
```
PS C:\> $VM = Get-AzureRMVM -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
PS C:\> Set-AzureRmVMDataDisk -VM $VM -Name "DataDisk01" -Caching ReadWrite | Update-AzureRmVM
```

<span data-ttu-id="fee73-111">첫 번째 명령은 **Get-AzureRmVM** 를 사용 하 여 ContosoVM07 이라는 가상 컴퓨터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fee73-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzureRmVM**.</span></span>
<span data-ttu-id="fee73-112">명령이 $VM 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="fee73-112">The command stores it in the $VM variable.</span></span>

<span data-ttu-id="fee73-113">두 번째 명령은 $VM의 가상 컴퓨터에서 DataDisk01 이라는 데이터 디스크에 대 한 캐싱 모드를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fee73-113">The second command modifies the caching mode for the data disk named DataDisk01 on the virtual machine in $VM.</span></span>
<span data-ttu-id="fee73-114">이 명령은 결과를 변경 내용을 구현 하는 Update-AzureRmVM cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="fee73-114">The command passes the result to the Update-AzureRmVM cmdlet, which implements your changes.</span></span>
<span data-ttu-id="fee73-115">캐싱 모드를 변경 하면 가상 컴퓨터가 다시 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fee73-115">A change to the caching mode causes the virtual machine to restart.</span></span>

## <span data-ttu-id="fee73-116">변수</span><span class="sxs-lookup"><span data-stu-id="fee73-116">PARAMETERS</span></span>

### <span data-ttu-id="fee73-117">-캐싱</span><span class="sxs-lookup"><span data-stu-id="fee73-117">-Caching</span></span>
<span data-ttu-id="fee73-118">디스크의 캐싱 모드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fee73-118">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="fee73-119">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="fee73-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fee73-120">읽기</span><span class="sxs-lookup"><span data-stu-id="fee73-120">ReadOnly</span></span>
- <span data-ttu-id="fee73-121">쓰기</span><span class="sxs-lookup"><span data-stu-id="fee73-121">ReadWrite</span></span>

<span data-ttu-id="fee73-122">기본값은 ReadWrite입니다.</span><span class="sxs-lookup"><span data-stu-id="fee73-122">The default value is ReadWrite.</span></span>
<span data-ttu-id="fee73-123">이 값을 변경 하면 가상 컴퓨터가 다시 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fee73-123">Changing this value causes the virtual machine to restart.</span></span>

<span data-ttu-id="fee73-124">이 설정은 디스크의 일관성 및 성능에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fee73-124">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="fee73-125">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="fee73-125">-DiskSizeInGB</span></span>
<span data-ttu-id="fee73-126">데이터 디스크의 크기 (기가바이트)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fee73-126">Specifies the size, in gigabytes, for the data disk.</span></span>

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

### <span data-ttu-id="fee73-127">-Lun</span><span class="sxs-lookup"><span data-stu-id="fee73-127">-Lun</span></span>
<span data-ttu-id="fee73-128">이 cmdlet이 수정 하는 데이터 디스크의 LUN (논리 단위 번호)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fee73-128">Specifies the logical unit number (LUN) of the data disk that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="fee73-129">-이름</span><span class="sxs-lookup"><span data-stu-id="fee73-129">-Name</span></span>
<span data-ttu-id="fee73-130">이 cmdlet이 수정 하는 데이터 디스크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fee73-130">Specifies the name of the data disk that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="fee73-131">-VM</span><span class="sxs-lookup"><span data-stu-id="fee73-131">-VM</span></span>
<span data-ttu-id="fee73-132">이 cmdlet이 데이터 디스크를 수정할 가상 컴퓨터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fee73-132">Specifies the virtual machine for which this cmdlet modifies a data disk.</span></span>
<span data-ttu-id="fee73-133">가상 컴퓨터 개체를 가져오려면 Get-AzureRmVM cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fee73-133">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="fee73-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fee73-134">CommonParameters</span></span>
<span data-ttu-id="fee73-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fee73-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fee73-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fee73-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fee73-137">입력</span><span class="sxs-lookup"><span data-stu-id="fee73-137">INPUTS</span></span>

### <span data-ttu-id="fee73-138">않아야</span><span class="sxs-lookup"><span data-stu-id="fee73-138">None</span></span>
<span data-ttu-id="fee73-139">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fee73-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fee73-140">출력</span><span class="sxs-lookup"><span data-stu-id="fee73-140">OUTPUTS</span></span>

## <span data-ttu-id="fee73-141">상속자</span><span class="sxs-lookup"><span data-stu-id="fee73-141">NOTES</span></span>

## <span data-ttu-id="fee73-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fee73-142">RELATED LINKS</span></span>

[<span data-ttu-id="fee73-143">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="fee73-143">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="fee73-144">업데이트-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="fee73-144">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


