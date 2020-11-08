---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F420A47F-D036-4B31-AA59-97CFC9C79E75
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4a53d0821832b29f0f1f6a0b2ab5f1353e3331a3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046198"
---
# <span data-ttu-id="4cd08-101">New-AzureVMImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="4cd08-101">New-AzureVMImageDiskConfigSet</span></span>

## <span data-ttu-id="4cd08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cd08-102">SYNOPSIS</span></span>
<span data-ttu-id="4cd08-103">디스크 구성 집합 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4cd08-103">Creates a disk configuration set object.</span></span>

## <span data-ttu-id="4cd08-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4cd08-104">SYNTAX</span></span>

```
New-AzureVMImageDiskConfigSet [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="4cd08-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4cd08-105">DESCRIPTION</span></span>
<span data-ttu-id="4cd08-106">**AzureVMImageDiskConfigSet** cmdlet은 image 업데이트 cmdlet에 전달 되는 디스크 구성 집합 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4cd08-106">The **New-AzureVMImageDiskConfigSet** cmdlet creates a disk configuration set object that is passed to the image update cmdlet.</span></span>
<span data-ttu-id="4cd08-107">이는 OSDiskConfig 및 DataDiskConfig 개체를 캡슐화 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cd08-107">It encapsulates the OSDiskConfig and the DataDiskConfig object.</span></span>
<span data-ttu-id="4cd08-108">**Set-AzureVMImageOSDiskConfig** 및 **set-AzureVMImageDataDiskConfig** cmdlet을 사용 하 여 가상 컴퓨터 이미지에 대 한 OS 디스크 및 데이터 디스크 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cd08-108">Use the **Set-AzureVMImageOSDiskConfig** and **Set-AzureVMImageDataDiskConfig** cmdlets to set the OS Disk and Data Disk properties for the virtual machine image.</span></span>

## <span data-ttu-id="4cd08-109">예제의</span><span class="sxs-lookup"><span data-stu-id="4cd08-109">EXAMPLES</span></span>

### <span data-ttu-id="4cd08-110">예제 1: 디스크 구성 집합 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="4cd08-110">Example 1: Create a disk configuration set object</span></span>
```
PS C:\> $Disk = New-AzureDiskConfigSet
PS C:\> $Disk = Set-AzureOSDiskConfig -DiskConfig $Disk -HostCaching ReadWrite
PS C:\> $Disk = Set-AzureDataDiskConfig -DiskConfig $Disk -Name "Test" -HostCaching "ReadWrite" -LUN 0
PS C:\> Update-AzureVMImage -ImageName "Image2" -Label "Test1" -Description "Test1" -DiskConfigSet $Disk;
```

<span data-ttu-id="4cd08-111">이 명령은 디스크 구성 집합 개체를 만들고 $Disk 이라는 변수에 결과를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cd08-111">This command creates a disk configuration set object and stores the results in the variable named $Disk.</span></span>
<span data-ttu-id="4cd08-112">디스크 구성을 만든 후에는 OSDiskConfig 및 DataDiskConfig를 설정 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4cd08-112">After the disk configuration is created, it is used to set the OSDiskConfig and DataDiskConfig.</span></span>
<span data-ttu-id="4cd08-113">그런 다음 가상 머신이 구성으로 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4cd08-113">Then the virtual machine is updated with the configuration.</span></span>

## <span data-ttu-id="4cd08-114">변수</span><span class="sxs-lookup"><span data-stu-id="4cd08-114">PARAMETERS</span></span>

### <span data-ttu-id="4cd08-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="4cd08-115">-InformationAction</span></span>
<span data-ttu-id="4cd08-116">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cd08-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="4cd08-117">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="4cd08-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4cd08-118">하기로</span><span class="sxs-lookup"><span data-stu-id="4cd08-118">Continue</span></span>
- <span data-ttu-id="4cd08-119">숨기기</span><span class="sxs-lookup"><span data-stu-id="4cd08-119">Ignore</span></span>
- <span data-ttu-id="4cd08-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="4cd08-120">Inquire</span></span>
- <span data-ttu-id="4cd08-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="4cd08-121">SilentlyContinue</span></span>
- <span data-ttu-id="4cd08-122">중지가</span><span class="sxs-lookup"><span data-stu-id="4cd08-122">Stop</span></span>
- <span data-ttu-id="4cd08-123">대기</span><span class="sxs-lookup"><span data-stu-id="4cd08-123">Suspend</span></span>

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

### <span data-ttu-id="4cd08-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4cd08-124">-InformationVariable</span></span>
<span data-ttu-id="4cd08-125">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cd08-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="4cd08-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cd08-126">CommonParameters</span></span>
<span data-ttu-id="4cd08-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cd08-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cd08-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cd08-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cd08-129">입력</span><span class="sxs-lookup"><span data-stu-id="4cd08-129">INPUTS</span></span>

## <span data-ttu-id="4cd08-130">출력</span><span class="sxs-lookup"><span data-stu-id="4cd08-130">OUTPUTS</span></span>

### <span data-ttu-id="4cd08-131">WindowsAzure. ServiceManagement. m m/. m a m 설정</span><span class="sxs-lookup"><span data-stu-id="4cd08-131">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="4cd08-132">상속자</span><span class="sxs-lookup"><span data-stu-id="4cd08-132">NOTES</span></span>

## <span data-ttu-id="4cd08-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4cd08-133">RELATED LINKS</span></span>

[<span data-ttu-id="4cd08-134">Get-AzureVMImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="4cd08-134">Get-AzureVMImageDiskConfigSet</span></span>](./Get-AzureVMImageDiskConfigSet.md)

[<span data-ttu-id="4cd08-135">Set-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="4cd08-135">Set-AzureVMImageOSDiskConfig</span></span>](./Set-AzureVMImageOSDiskConfig.md)

[<span data-ttu-id="4cd08-136">Set-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="4cd08-136">Set-AzureVMImageDataDiskConfig</span></span>](./Set-AzureVMImageDataDiskConfig.md)


