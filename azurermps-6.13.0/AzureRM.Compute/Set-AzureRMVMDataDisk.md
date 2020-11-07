---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: C453485D-67A7-480E-83F6-527D4F5EBC93
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRMVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRMVMDataDisk.md
ms.openlocfilehash: 4ed0abb355bf7a755e5acaa36f8bb11e88d80c5c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702626"
---
# <span data-ttu-id="0c9f6-101">Set-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="0c9f6-101">Set-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="0c9f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c9f6-102">SYNOPSIS</span></span>
<span data-ttu-id="0c9f6-103">가상 컴퓨터 데이터 디스크의 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c9f6-103">Modifies properties of a virtual machine data disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c9f6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0c9f6-104">SYNTAX</span></span>

### <span data-ttu-id="0c9f6-105">ChangeWithName</span><span class="sxs-lookup"><span data-stu-id="0c9f6-105">ChangeWithName</span></span>
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Name] <String> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c9f6-106">ChangeWithLun</span><span class="sxs-lookup"><span data-stu-id="0c9f6-106">ChangeWithLun</span></span>
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Lun] <Int32> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c9f6-107">설명은</span><span class="sxs-lookup"><span data-stu-id="0c9f6-107">DESCRIPTION</span></span>
<span data-ttu-id="0c9f6-108">**AzureRmVMDataDisk** cmdlet은 가상 컴퓨터 데이터 디스크의 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c9f6-108">The **Set-AzureRmVMDataDisk** cmdlet modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="0c9f6-109">예제의</span><span class="sxs-lookup"><span data-stu-id="0c9f6-109">EXAMPLES</span></span>

### <span data-ttu-id="0c9f6-110">예제 1: 데이터 디스크의 캐싱 모드 수정</span><span class="sxs-lookup"><span data-stu-id="0c9f6-110">Example 1: Modify the caching mode of a data disk</span></span>
```
PS C:\> $VM = Get-AzureRMVM -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
PS C:\> Set-AzureRmVMDataDisk -VM $VM -Name "DataDisk01" -Caching ReadWrite | Update-AzureRmVM
```

<span data-ttu-id="0c9f6-111">첫 번째 명령은 **Get-AzureRmVM** 를 사용 하 여 ContosoVM07 이라는 가상 컴퓨터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0c9f6-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzureRmVM**.</span></span>
<span data-ttu-id="0c9f6-112">명령이 $VM 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c9f6-112">The command stores it in the $VM variable.</span></span>
<span data-ttu-id="0c9f6-113">두 번째 명령은 $VM의 가상 컴퓨터에서 DataDisk01 이라는 데이터 디스크에 대 한 캐싱 모드를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c9f6-113">The second command modifies the caching mode for the data disk named DataDisk01 on the virtual machine in $VM.</span></span>
<span data-ttu-id="0c9f6-114">이 명령은 결과를 변경 내용을 구현 하는 Update-AzureRmVM cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c9f6-114">The command passes the result to the Update-AzureRmVM cmdlet, which implements your changes.</span></span>
<span data-ttu-id="0c9f6-115">Cashing mode를 변경 하면 가상 컴퓨터가 다시 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0c9f6-115">A change to the cashing mode causes the virtual machine to restart.</span></span>

## <span data-ttu-id="0c9f6-116">변수</span><span class="sxs-lookup"><span data-stu-id="0c9f6-116">PARAMETERS</span></span>

### <span data-ttu-id="0c9f6-117">-캐싱</span><span class="sxs-lookup"><span data-stu-id="0c9f6-117">-Caching</span></span>
<span data-ttu-id="0c9f6-118">디스크의 캐싱 모드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c9f6-118">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="0c9f6-119">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0c9f6-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0c9f6-120">읽기</span><span class="sxs-lookup"><span data-stu-id="0c9f6-120">ReadOnly</span></span>
- <span data-ttu-id="0c9f6-121">ReadWrite 기본값은 ReadWrite입니다.</span><span class="sxs-lookup"><span data-stu-id="0c9f6-121">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="0c9f6-122">이 값을 변경 하면 가상 컴퓨터가 다시 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0c9f6-122">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="0c9f6-123">이 설정은 디스크의 일관성 및 성능에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0c9f6-123">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="0c9f6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c9f6-124">-DefaultProfile</span></span>
<span data-ttu-id="0c9f6-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0c9f6-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c9f6-126">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="0c9f6-126">-DiskSizeInGB</span></span>
<span data-ttu-id="0c9f6-127">데이터 디스크의 크기 (기가바이트)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c9f6-127">Specifies the size, in gigabytes, for the data disk.</span></span>

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

### <span data-ttu-id="0c9f6-128">-Lun</span><span class="sxs-lookup"><span data-stu-id="0c9f6-128">-Lun</span></span>
<span data-ttu-id="0c9f6-129">이 cmdlet이 수정 하는 데이터 디스크의 LUN (논리 단위 번호)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c9f6-129">Specifies the logical unit number (LUN) of the data disk that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="0c9f6-130">-이름</span><span class="sxs-lookup"><span data-stu-id="0c9f6-130">-Name</span></span>
<span data-ttu-id="0c9f6-131">이 cmdlet이 수정 하는 데이터 디스크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c9f6-131">Specifies the name of the data disk that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="0c9f6-132">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="0c9f6-132">-StorageAccountType</span></span>
<span data-ttu-id="0c9f6-133">가상 컴퓨터 관리 디스크의 계정 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="0c9f6-133">The virtual machine managed disk's account type.</span></span>

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

### <span data-ttu-id="0c9f6-134">-VM</span><span class="sxs-lookup"><span data-stu-id="0c9f6-134">-VM</span></span>
<span data-ttu-id="0c9f6-135">이 cmdlet이 데이터 디스크를 수정할 가상 컴퓨터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c9f6-135">Specifies the virtual machine for which this cmdlet modifies a data disk.</span></span>
<span data-ttu-id="0c9f6-136">가상 컴퓨터 개체를 가져오려면 Get-AzureRmVM cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c9f6-136">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="0c9f6-137">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="0c9f6-137">-WriteAccelerator</span></span>
<span data-ttu-id="0c9f6-138">데이터 디스크에서 WriteAccelerator를 사용할지 아니면 disabled를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c9f6-138">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

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

### <span data-ttu-id="0c9f6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c9f6-139">CommonParameters</span></span>
<span data-ttu-id="0c9f6-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c9f6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c9f6-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c9f6-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c9f6-142">입력</span><span class="sxs-lookup"><span data-stu-id="0c9f6-142">INPUTS</span></span>

### <span data-ttu-id="0c9f6-143">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c9f6-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="0c9f6-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0c9f6-144">System.String</span></span>

### <span data-ttu-id="0c9f6-145">시스템 Null 허용 ' 1 [[b77a5c561934e089, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken =]]</span><span class="sxs-lookup"><span data-stu-id="0c9f6-145">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="0c9f6-146">시스템 Null 허용 ' 1 [[21.0.0.0], [[Microsoft Azure. 31bf3856ad364e35.-Management. 관리. t e;. i =, Culture = 중립, PublicKeyToken =]]</span><span class="sxs-lookup"><span data-stu-id="0c9f6-146">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="0c9f6-147">출력</span><span class="sxs-lookup"><span data-stu-id="0c9f6-147">OUTPUTS</span></span>

### <span data-ttu-id="0c9f6-148">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c9f6-148">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="0c9f6-149">상속자</span><span class="sxs-lookup"><span data-stu-id="0c9f6-149">NOTES</span></span>

## <span data-ttu-id="0c9f6-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0c9f6-150">RELATED LINKS</span></span>

[<span data-ttu-id="0c9f6-151">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="0c9f6-151">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="0c9f6-152">업데이트-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="0c9f6-152">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


