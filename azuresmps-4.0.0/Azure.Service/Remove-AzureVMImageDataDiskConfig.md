---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5CAF2D29-F4AE-4322-AA4F-61267723B955
online version: ''
schema: 2.0.0
ms.openlocfilehash: b2e19ad4b56e5141458f1fe9305a0c33691d024d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045497"
---
# <span data-ttu-id="4b875-101">Remove-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="4b875-101">Remove-AzureVMImageDataDiskConfig</span></span>

## <span data-ttu-id="4b875-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b875-102">SYNOPSIS</span></span>
<span data-ttu-id="4b875-103">DiskConfigSet 개체에서 데이터 디스크 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b875-103">Removes the data disk configuration from the DiskConfigSet object.</span></span>

## <span data-ttu-id="4b875-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4b875-104">SYNTAX</span></span>

### <span data-ttu-id="4b875-105">RemoveByDiskName (기본값)</span><span class="sxs-lookup"><span data-stu-id="4b875-105">RemoveByDiskName (Default)</span></span>
```
Remove-AzureVMImageDataDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [-DataDiskName] <String>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="4b875-106">RemoveByDiskLun</span><span class="sxs-lookup"><span data-stu-id="4b875-106">RemoveByDiskLun</span></span>
```
Remove-AzureVMImageDataDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [-Lun] <Int32>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="4b875-107">설명은</span><span class="sxs-lookup"><span data-stu-id="4b875-107">DESCRIPTION</span></span>
<span data-ttu-id="4b875-108">**AzureVMImageDataDiskConfig** Cmdlet은 **diskconfigset** 개체에서 데이터 디스크 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b875-108">The **Remove-AzureVMImageDataDiskConfig** cmdlet removes the data disk configuration from the **DiskConfigSet** object.</span></span>

## <span data-ttu-id="4b875-109">예제의</span><span class="sxs-lookup"><span data-stu-id="4b875-109">EXAMPLES</span></span>

### <span data-ttu-id="4b875-110">예제 1: DiskConfigSet 개체에서 데이터 디스크 구성 제거</span><span class="sxs-lookup"><span data-stu-id="4b875-110">Example 1: Remove the data disk configuration from the DiskConfigSet object</span></span>
```
PS C:\> $Disk = New-AzureDiskConfigSet
PS C:\> $Disk = Set-AzureDataDiskConfig -DiskConfig $Disk -HostCaching ReadWrite
PS C:\> Remove-AzureVMImageDataDiskConfig -DiskConfig $Disk
```

<span data-ttu-id="4b875-111">이 예제에서는 **Diskconfigset** 을 만들어 구성한 다음 데이터 디스크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b875-111">This example creates a **DiskConfigSet** , configures it, then removes the data disk.</span></span>

## <span data-ttu-id="4b875-112">변수</span><span class="sxs-lookup"><span data-stu-id="4b875-112">PARAMETERS</span></span>

### <span data-ttu-id="4b875-113">-DataDiskName</span><span class="sxs-lookup"><span data-stu-id="4b875-113">-DataDiskName</span></span>
<span data-ttu-id="4b875-114">이 cmdlet이 제거 하는 데이터 디스크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b875-114">Specifies the name of the data disk that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByDiskName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b875-115">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="4b875-115">-DiskConfig</span></span>
<span data-ttu-id="4b875-116">운영 체제 디스크 및 데이터 디스크 개체를 캡슐화 하는 디스크 구성 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b875-116">Specifies the disk configuration object that encapsulates the operating system disk and data disk objects.</span></span>

```yaml
Type: VirtualMachineImageDiskConfigSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4b875-117">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="4b875-117">-InformationAction</span></span>
<span data-ttu-id="4b875-118">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b875-118">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="4b875-119">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="4b875-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4b875-120">하기로</span><span class="sxs-lookup"><span data-stu-id="4b875-120">Continue</span></span>
- <span data-ttu-id="4b875-121">숨기기</span><span class="sxs-lookup"><span data-stu-id="4b875-121">Ignore</span></span>
- <span data-ttu-id="4b875-122">Inquire</span><span class="sxs-lookup"><span data-stu-id="4b875-122">Inquire</span></span>
- <span data-ttu-id="4b875-123">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="4b875-123">SilentlyContinue</span></span>
- <span data-ttu-id="4b875-124">중지가</span><span class="sxs-lookup"><span data-stu-id="4b875-124">Stop</span></span>
- <span data-ttu-id="4b875-125">대기</span><span class="sxs-lookup"><span data-stu-id="4b875-125">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b875-126">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4b875-126">-InformationVariable</span></span>
<span data-ttu-id="4b875-127">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b875-127">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b875-128">-Lun</span><span class="sxs-lookup"><span data-stu-id="4b875-128">-Lun</span></span>
<span data-ttu-id="4b875-129">가상 컴퓨터에서 데이터 드라이브가 탑재 된 슬롯을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b875-129">Specifies the slot where the data drive is mounted in the virtual machine.</span></span>

```yaml
Type: Int32
Parameter Sets: RemoveByDiskLun
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b875-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b875-130">CommonParameters</span></span>
<span data-ttu-id="4b875-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b875-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b875-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b875-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b875-133">입력</span><span class="sxs-lookup"><span data-stu-id="4b875-133">INPUTS</span></span>

## <span data-ttu-id="4b875-134">출력</span><span class="sxs-lookup"><span data-stu-id="4b875-134">OUTPUTS</span></span>

### <span data-ttu-id="4b875-135">WindowsAzure. ServiceManagement. m m/. m a m 설정</span><span class="sxs-lookup"><span data-stu-id="4b875-135">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="4b875-136">상속자</span><span class="sxs-lookup"><span data-stu-id="4b875-136">NOTES</span></span>

## <span data-ttu-id="4b875-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4b875-137">RELATED LINKS</span></span>

[<span data-ttu-id="4b875-138">Set-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="4b875-138">Set-AzureVMImageDataDiskConfig</span></span>](./Set-AzureVMImageDataDiskConfig.md)


