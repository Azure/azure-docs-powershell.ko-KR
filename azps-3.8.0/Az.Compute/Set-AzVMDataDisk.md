---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C453485D-67A7-480E-83F6-527D4F5EBC93
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDataDisk.md
ms.openlocfilehash: 2361fc663efc3ec4a967c718abd778599ca5340b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044639"
---
# <span data-ttu-id="0e438-101">Set-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="0e438-101">Set-AzVMDataDisk</span></span>

## <span data-ttu-id="0e438-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e438-102">SYNOPSIS</span></span>
<span data-ttu-id="0e438-103">가상 컴퓨터 데이터 디스크의 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e438-103">Modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="0e438-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0e438-104">SYNTAX</span></span>

### <span data-ttu-id="0e438-105">ChangeWithName</span><span class="sxs-lookup"><span data-stu-id="0e438-105">ChangeWithName</span></span>
```
Set-AzVMDataDisk [-VM] <PSVirtualMachine> [-Name] <String> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e438-106">ChangeWithLun</span><span class="sxs-lookup"><span data-stu-id="0e438-106">ChangeWithLun</span></span>
```
Set-AzVMDataDisk [-VM] <PSVirtualMachine> [-Lun] <Int32> [[-Caching] <CachingTypes>] [[-DiskSizeInGB] <Int32>]
 [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e438-107">설명은</span><span class="sxs-lookup"><span data-stu-id="0e438-107">DESCRIPTION</span></span>
<span data-ttu-id="0e438-108">**AzVMDataDisk** cmdlet은 가상 컴퓨터 데이터 디스크의 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e438-108">The **Set-AzVMDataDisk** cmdlet modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="0e438-109">예제의</span><span class="sxs-lookup"><span data-stu-id="0e438-109">EXAMPLES</span></span>

### <span data-ttu-id="0e438-110">예제 1: 데이터 디스크의 캐싱 모드 수정</span><span class="sxs-lookup"><span data-stu-id="0e438-110">Example 1: Modify the caching mode of a data disk</span></span>
```
PS C:\> $VM = Get-AzVM -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
PS C:\> Set-AzVMDataDisk -VM $VM -Name "DataDisk01" -Caching ReadWrite | Update-AzVM
```

<span data-ttu-id="0e438-111">첫 번째 명령은 **Get-AzVM** 를 사용 하 여 ContosoVM07 이라는 가상 컴퓨터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0e438-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzVM**.</span></span>
<span data-ttu-id="0e438-112">명령이 $VM 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e438-112">The command stores it in the $VM variable.</span></span>
<span data-ttu-id="0e438-113">두 번째 명령은 $VM의 가상 컴퓨터에서 DataDisk01 이라는 데이터 디스크에 대 한 캐싱 모드를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e438-113">The second command modifies the caching mode for the data disk named DataDisk01 on the virtual machine in $VM.</span></span>
<span data-ttu-id="0e438-114">이 명령은 결과를 변경 내용을 구현 하는 Update-AzVM cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e438-114">The command passes the result to the Update-AzVM cmdlet, which implements your changes.</span></span>
<span data-ttu-id="0e438-115">Cashing mode를 변경 하면 가상 컴퓨터가 다시 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e438-115">A change to the cashing mode causes the virtual machine to restart.</span></span>

## <span data-ttu-id="0e438-116">변수</span><span class="sxs-lookup"><span data-stu-id="0e438-116">PARAMETERS</span></span>

### <span data-ttu-id="0e438-117">-캐싱</span><span class="sxs-lookup"><span data-stu-id="0e438-117">-Caching</span></span>
<span data-ttu-id="0e438-118">디스크의 캐싱 모드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e438-118">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="0e438-119">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0e438-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0e438-120">읽기</span><span class="sxs-lookup"><span data-stu-id="0e438-120">ReadOnly</span></span>
- <span data-ttu-id="0e438-121">ReadWrite 기본값은 ReadWrite입니다.</span><span class="sxs-lookup"><span data-stu-id="0e438-121">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="0e438-122">이 값을 변경 하면 가상 컴퓨터가 다시 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e438-122">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="0e438-123">이 설정은 디스크의 일관성 및 성능에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0e438-123">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e438-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e438-124">-DefaultProfile</span></span>
<span data-ttu-id="0e438-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0e438-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e438-126">-Disk. Setid</span><span class="sxs-lookup"><span data-stu-id="0e438-126">-DiskEncryptionSetId</span></span>
<span data-ttu-id="0e438-127">고객 관리 디스크 암호화 집합의 리소스 Id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e438-127">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="0e438-128">이는 관리 디스크에 대해서만 지정 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e438-128">This can only be specified for managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e438-129">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="0e438-129">-DiskSizeInGB</span></span>
<span data-ttu-id="0e438-130">데이터 디스크의 크기 (기가바이트)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e438-130">Specifies the size, in gigabytes, for the data disk.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e438-131">-Lun</span><span class="sxs-lookup"><span data-stu-id="0e438-131">-Lun</span></span>
<span data-ttu-id="0e438-132">이 cmdlet이 수정 하는 데이터 디스크의 LUN (논리 단위 번호)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e438-132">Specifies the logical unit number (LUN) of the data disk that this cmdlet modifies.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ChangeWithLun
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e438-133">-이름</span><span class="sxs-lookup"><span data-stu-id="0e438-133">-Name</span></span>
<span data-ttu-id="0e438-134">이 cmdlet이 수정 하는 데이터 디스크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e438-134">Specifies the name of the data disk that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ChangeWithName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e438-135">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="0e438-135">-StorageAccountType</span></span>
<span data-ttu-id="0e438-136">가상 컴퓨터 관리 디스크의 계정 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="0e438-136">The virtual machine managed disk's account type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e438-137">-VM</span><span class="sxs-lookup"><span data-stu-id="0e438-137">-VM</span></span>
<span data-ttu-id="0e438-138">이 cmdlet이 데이터 디스크를 수정할 가상 컴퓨터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e438-138">Specifies the virtual machine for which this cmdlet modifies a data disk.</span></span>
<span data-ttu-id="0e438-139">가상 컴퓨터 개체를 가져오려면 Get-AzVM cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e438-139">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0e438-140">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="0e438-140">-WriteAccelerator</span></span>
<span data-ttu-id="0e438-141">데이터 디스크에서 WriteAccelerator를 사용할지 아니면 disabled를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e438-141">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

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

### <span data-ttu-id="0e438-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e438-142">CommonParameters</span></span>
<span data-ttu-id="0e438-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e438-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e438-144">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0e438-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e438-145">입력</span><span class="sxs-lookup"><span data-stu-id="0e438-145">INPUTS</span></span>

### <span data-ttu-id="0e438-146">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e438-146">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="0e438-147">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0e438-147">System.String</span></span>

### <span data-ttu-id="0e438-148">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e])</span><span class="sxs-lookup"><span data-stu-id="0e438-148">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="0e438-149">시스템 Null 허용 ' 1 [[23.0.0.0], [[Microsoft Azure. 31bf3856ad364e35.-Management. 관리. t e;. i =, Culture = 중립, PublicKeyToken =]]</span><span class="sxs-lookup"><span data-stu-id="0e438-149">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="0e438-150">출력</span><span class="sxs-lookup"><span data-stu-id="0e438-150">OUTPUTS</span></span>

### <span data-ttu-id="0e438-151">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e438-151">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="0e438-152">상속자</span><span class="sxs-lookup"><span data-stu-id="0e438-152">NOTES</span></span>

## <span data-ttu-id="0e438-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0e438-153">RELATED LINKS</span></span>

[<span data-ttu-id="0e438-154">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="0e438-154">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="0e438-155">업데이트-AzVM</span><span class="sxs-lookup"><span data-stu-id="0e438-155">Update-AzVM</span></span>](./Update-AzVM.md)


