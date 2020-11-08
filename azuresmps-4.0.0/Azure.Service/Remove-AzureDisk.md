---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 75A50C59-28D1-4D29-A420-D24BF479F79E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 29e5e7e0bc2fcc0ce93186cf966f18d6c9c3e372
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046157"
---
# <span data-ttu-id="3c13a-101">Remove-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="3c13a-101">Remove-AzureDisk</span></span>

## <span data-ttu-id="3c13a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c13a-102">SYNOPSIS</span></span>
<span data-ttu-id="3c13a-103">Azure 디스크 리포지토리에서 디스크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c13a-103">Removes a disk from the Azure disk repository.</span></span>

## <span data-ttu-id="3c13a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3c13a-104">SYNTAX</span></span>

```
Remove-AzureDisk [-DiskName] <String> [-DeleteVHD] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="3c13a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3c13a-105">DESCRIPTION</span></span>
<span data-ttu-id="3c13a-106">**제거-azuredisk** cmdlet는 현재 구독의 Azure 디스크 리포지토리에서 디스크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c13a-106">The **Remove-AzureDisk** cmdlet removes a disk from the Azure disk repository in the current subscription.</span></span>
<span data-ttu-id="3c13a-107">기본적으로이 cmdlet은 blob 저장소에서 VHD (가상 하드 디스크) 파일을 삭제 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3c13a-107">By default, this cmdlet does not delete the virtual hard disk (VHD) file from blob storage.</span></span>
<span data-ttu-id="3c13a-108">VHD를 삭제 하려면 *Deletevhd* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c13a-108">To delete the VHD, specify the *DeleteVHD* parameter.</span></span>

## <span data-ttu-id="3c13a-109">예제의</span><span class="sxs-lookup"><span data-stu-id="3c13a-109">EXAMPLES</span></span>

### <span data-ttu-id="3c13a-110">예제 1: 디스크 제거</span><span class="sxs-lookup"><span data-stu-id="3c13a-110">Example 1: Remove a disk</span></span>
```
PS C:\> Remove-AzureDisk -DiskName "ContosoDataDisk"
```

<span data-ttu-id="3c13a-111">이 명령은 디스크 리포지토리에서 ContosoDataDisk disk 라는 디스크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c13a-111">This command removes the disk named ContosoDataDisk disk from the disk repository.</span></span>
<span data-ttu-id="3c13a-112">이 명령은 VHD를 삭제 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3c13a-112">The command does not delete the VHD.</span></span>

### <span data-ttu-id="3c13a-113">예제 2: 디스크 제거 및 삭제</span><span class="sxs-lookup"><span data-stu-id="3c13a-113">Example 2: Remove and delete a disk</span></span>
```
PS C:\> Remove-AzureDisk -DiskName "ContosoDataDisk" -DeleteVHD
```

<span data-ttu-id="3c13a-114">이 명령은 디스크 리포지토리에서 ContosoDataDisk disk 라는 디스크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c13a-114">This command removes the disk named ContosoDataDisk disk from the disk repository.</span></span>
<span data-ttu-id="3c13a-115">이 명령은 DeleteVHD 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c13a-115">This command specifies the DeleteVHD parameter.</span></span>
<span data-ttu-id="3c13a-116">따라서 명령은 Azure 저장소에서 VHD를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c13a-116">Therefore, the command deletes the VHD from Azure Storage.</span></span>

## <span data-ttu-id="3c13a-117">변수</span><span class="sxs-lookup"><span data-stu-id="3c13a-117">PARAMETERS</span></span>

### <span data-ttu-id="3c13a-118">-DeleteVHD</span><span class="sxs-lookup"><span data-stu-id="3c13a-118">-DeleteVHD</span></span>
<span data-ttu-id="3c13a-119">이 cmdlet이 blob 저장소에서 VHD를 제거 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3c13a-119">Indicates that this cmdlet removes the VHD from blob storage.</span></span>

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

### <span data-ttu-id="3c13a-120">-DiskName</span><span class="sxs-lookup"><span data-stu-id="3c13a-120">-DiskName</span></span>
<span data-ttu-id="3c13a-121">이 cmdlet이 제거 하는 디스크 리포지토리에서 데이터 디스크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c13a-121">Specifies the name of the data disk in the disk repository that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c13a-122">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="3c13a-122">-InformationAction</span></span>
<span data-ttu-id="3c13a-123">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c13a-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3c13a-124">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="3c13a-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3c13a-125">하기로</span><span class="sxs-lookup"><span data-stu-id="3c13a-125">Continue</span></span>
- <span data-ttu-id="3c13a-126">숨기기</span><span class="sxs-lookup"><span data-stu-id="3c13a-126">Ignore</span></span>
- <span data-ttu-id="3c13a-127">Inquire</span><span class="sxs-lookup"><span data-stu-id="3c13a-127">Inquire</span></span>
- <span data-ttu-id="3c13a-128">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3c13a-128">SilentlyContinue</span></span>
- <span data-ttu-id="3c13a-129">중지가</span><span class="sxs-lookup"><span data-stu-id="3c13a-129">Stop</span></span>
- <span data-ttu-id="3c13a-130">대기</span><span class="sxs-lookup"><span data-stu-id="3c13a-130">Suspend</span></span>

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

### <span data-ttu-id="3c13a-131">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3c13a-131">-InformationVariable</span></span>
<span data-ttu-id="3c13a-132">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c13a-132">Specifies an information variable.</span></span>

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

### <span data-ttu-id="3c13a-133">-프로필</span><span class="sxs-lookup"><span data-stu-id="3c13a-133">-Profile</span></span>
<span data-ttu-id="3c13a-134">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c13a-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3c13a-135">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="3c13a-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c13a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c13a-136">CommonParameters</span></span>
<span data-ttu-id="3c13a-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c13a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c13a-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c13a-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c13a-139">입력</span><span class="sxs-lookup"><span data-stu-id="3c13a-139">INPUTS</span></span>

## <span data-ttu-id="3c13a-140">출력</span><span class="sxs-lookup"><span data-stu-id="3c13a-140">OUTPUTS</span></span>

## <span data-ttu-id="3c13a-141">상속자</span><span class="sxs-lookup"><span data-stu-id="3c13a-141">NOTES</span></span>

## <span data-ttu-id="3c13a-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3c13a-142">RELATED LINKS</span></span>

[<span data-ttu-id="3c13a-143">추가-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="3c13a-143">Add-AzureDisk</span></span>](./Add-AzureDisk.md)

[<span data-ttu-id="3c13a-144">Get-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="3c13a-144">Get-AzureDisk</span></span>](./Get-AzureDisk.md)

[<span data-ttu-id="3c13a-145">업데이트-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="3c13a-145">Update-AzureDisk</span></span>](./Update-AzureDisk.md)


