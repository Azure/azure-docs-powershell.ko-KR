---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1E1F98E9-FC45-4BEF-90F6-A21D7DB7C82F
online version: ''
schema: 2.0.0
ms.openlocfilehash: eac6db4400e5c51f295e0bbf549117ffdbc97644
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046445"
---
# <span data-ttu-id="27263-101">Remove-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="27263-101">Remove-AzureVMImageOSDiskConfig</span></span>

## <span data-ttu-id="27263-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27263-102">SYNOPSIS</span></span>
<span data-ttu-id="27263-103">DiskConfigSet 개체에서 운영 체제 디스크 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="27263-103">Removes the operating system disk configuration from the DiskConfigSet object.</span></span>

## <span data-ttu-id="27263-104">구문과</span><span class="sxs-lookup"><span data-stu-id="27263-104">SYNTAX</span></span>

```
Remove-AzureVMImageOSDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="27263-105">설명은</span><span class="sxs-lookup"><span data-stu-id="27263-105">DESCRIPTION</span></span>
<span data-ttu-id="27263-106">**AzureVMImageOSDiskConfig** Cmdlet은 DiskConfigSet 개체에서 운영 체제 디스크 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="27263-106">The **Remove-AzureVMImageOSDiskConfig** cmdlet removes the operating system disk configuration from the DiskConfigSet object.</span></span>

## <span data-ttu-id="27263-107">예제의</span><span class="sxs-lookup"><span data-stu-id="27263-107">EXAMPLES</span></span>

### <span data-ttu-id="27263-108">예제 1: DiskConfigSet에서 운영 체제 디스크 구성 제거</span><span class="sxs-lookup"><span data-stu-id="27263-108">Example 1: Remove the operating system disk configuration from a DiskConfigSet</span></span>
```
PS C:\> $Disk = New-AzureDiskConfigSet
PS C:\> $Disk = Set-AzureOSDiskConfig -DiskConfig $Disk -HostCaching ReadWrite
PS C:\> Remove-AzureVMImageOSDiskConfig -DiskConfig $Disk
```

<span data-ttu-id="27263-109">이 명령은 DiskConfigSet 개체에서 운영 체제 디스크 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="27263-109">This command removes the operating system disk configuration from the DiskConfigSet object</span></span>

## <span data-ttu-id="27263-110">변수</span><span class="sxs-lookup"><span data-stu-id="27263-110">PARAMETERS</span></span>

### <span data-ttu-id="27263-111">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="27263-111">-DiskConfig</span></span>
<span data-ttu-id="27263-112">운영 체제 디스크 및 데이터 디스크 개체를 캡슐화 하는 디스크 구성 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="27263-112">Specifies the disk configuration object that encapsulates the operating system disk and Data Disk objects.</span></span>

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

### <span data-ttu-id="27263-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="27263-113">-InformationAction</span></span>
<span data-ttu-id="27263-114">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="27263-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="27263-115">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="27263-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="27263-116">하기로</span><span class="sxs-lookup"><span data-stu-id="27263-116">Continue</span></span>
- <span data-ttu-id="27263-117">숨기기</span><span class="sxs-lookup"><span data-stu-id="27263-117">Ignore</span></span>
- <span data-ttu-id="27263-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="27263-118">Inquire</span></span>
- <span data-ttu-id="27263-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="27263-119">SilentlyContinue</span></span>
- <span data-ttu-id="27263-120">중지가</span><span class="sxs-lookup"><span data-stu-id="27263-120">Stop</span></span>
- <span data-ttu-id="27263-121">대기</span><span class="sxs-lookup"><span data-stu-id="27263-121">Suspend</span></span>

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

### <span data-ttu-id="27263-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="27263-122">-InformationVariable</span></span>
<span data-ttu-id="27263-123">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="27263-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="27263-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27263-124">CommonParameters</span></span>
<span data-ttu-id="27263-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="27263-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27263-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27263-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27263-127">입력</span><span class="sxs-lookup"><span data-stu-id="27263-127">INPUTS</span></span>

## <span data-ttu-id="27263-128">출력</span><span class="sxs-lookup"><span data-stu-id="27263-128">OUTPUTS</span></span>

### <span data-ttu-id="27263-129">WindowsAzure. ServiceManagement. m m/. m a m 설정</span><span class="sxs-lookup"><span data-stu-id="27263-129">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="27263-130">상속자</span><span class="sxs-lookup"><span data-stu-id="27263-130">NOTES</span></span>

## <span data-ttu-id="27263-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="27263-131">RELATED LINKS</span></span>

[<span data-ttu-id="27263-132">Set-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="27263-132">Set-AzureVMImageOSDiskConfig</span></span>](./Set-AzureVMImageOSDiskConfig.md)


