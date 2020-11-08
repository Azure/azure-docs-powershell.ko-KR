---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 95DCD2EC-8327-4A46-B624-289D0A28F7EA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4614910b8c0ccd36bb8ef75ee98f662cf69a276a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046354"
---
# <span data-ttu-id="08116-101">Get-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="08116-101">Get-AzureDisk</span></span>

## <span data-ttu-id="08116-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08116-102">SYNOPSIS</span></span>
<span data-ttu-id="08116-103">Azure 디스크 리포지토리의 디스크에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="08116-103">Gets information about disks in the Azure disk repository.</span></span>

## <span data-ttu-id="08116-104">구문과</span><span class="sxs-lookup"><span data-stu-id="08116-104">SYNTAX</span></span>

```
Get-AzureDisk [[-DiskName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="08116-105">설명은</span><span class="sxs-lookup"><span data-stu-id="08116-105">DESCRIPTION</span></span>
<span data-ttu-id="08116-106">**Get AzureDisk** cmdlet은 현재 구독에 대 한 Azure 디스크 리포지토리에 저장 된 디스크에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="08116-106">The **Get-AzureDisk** cmdlet gets information about the disks that are stored in the Azure disk repository for the current subscription.</span></span>
<span data-ttu-id="08116-107">이 cmdlet은 리포지토리의 모든 디스크에 대 한 정보 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="08116-107">This cmdlet returns a list of information for all disks in the repository.</span></span>
<span data-ttu-id="08116-108">특정 디스크에 대 한 정보를 보려면 디스크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="08116-108">To view information for a specific disk, specify the name of the disk.</span></span>

## <span data-ttu-id="08116-109">예제의</span><span class="sxs-lookup"><span data-stu-id="08116-109">EXAMPLES</span></span>

### <span data-ttu-id="08116-110">예제 1: 디스크에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="08116-110">Example 1: Get information about a disk</span></span>
```
PS C:\> Get-AzureDisk -DiskName "ContosoDataDisk"
```

<span data-ttu-id="08116-111">이 명령은 디스크 리포지토리에서 ContosoDataDisk 이라는 디스크에 대 한 정보 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="08116-111">This command gets information data about the disk named ContosoDataDisk from the disk repository.</span></span>

### <span data-ttu-id="08116-112">예제 2: 모든 디스크에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="08116-112">Example 2: Get information about all disks</span></span>
```
PS C:\> Get-AzureDisk
```

<span data-ttu-id="08116-113">이 명령은 디스크 리포지토리의 모든 디스크에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="08116-113">This command gets information about all the disks in the disk repository.</span></span>

### <span data-ttu-id="08116-114">예제 3: 디스크에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="08116-114">Example 3: Get information about a disk</span></span>
```
PS C:\> Get-AzureDisk | Where-Object {$_.AttachedTo -eq $Null } | Format-Table -AutoSize -Property "DiskName","DiskSizeInGB","MediaLink"
```

<span data-ttu-id="08116-115">이 명령은 현재 가상 컴퓨터에 연결 되어 있지 않은 디스크 리포지토리의 모든 디스크에 대 한 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="08116-115">This command gets data for all of the disks in the disk repository that are not currently attached to a virtual machine.</span></span>
<span data-ttu-id="08116-116">명령은 모든 디스크에 대 한 정보를 가져오고 각 개체를 **Where-object** cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="08116-116">The command gets information about all of the disks, and passes each object to the **Where-Object** cmdlet.</span></span>
<span data-ttu-id="08116-117">해당 cmdlet은 **AttachedTo** 속성에 대 한 $Null 값이 없는 모든 디스크를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="08116-117">That cmdlet drops any disk that does not have a value of $Null for the **AttachedTo** property.</span></span>
<span data-ttu-id="08116-118">명령은 **Format 테이블** cmdlet을 사용 하 여 목록의 형식을 표로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="08116-118">The command formats the list as a table by using the **Format-Table** cmdlet.</span></span>

## <span data-ttu-id="08116-119">변수</span><span class="sxs-lookup"><span data-stu-id="08116-119">PARAMETERS</span></span>

### <span data-ttu-id="08116-120">-DiskName</span><span class="sxs-lookup"><span data-stu-id="08116-120">-DiskName</span></span>
<span data-ttu-id="08116-121">이 cmdlet에 대 한 정보를 가져오는 디스크 리포지토리의 디스크 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="08116-121">Specifies the name of the disk in the disk repository about which this cmdlet gets information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08116-122">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="08116-122">-InformationAction</span></span>
<span data-ttu-id="08116-123">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="08116-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="08116-124">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="08116-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="08116-125">하기로</span><span class="sxs-lookup"><span data-stu-id="08116-125">Continue</span></span>
- <span data-ttu-id="08116-126">숨기기</span><span class="sxs-lookup"><span data-stu-id="08116-126">Ignore</span></span>
- <span data-ttu-id="08116-127">Inquire</span><span class="sxs-lookup"><span data-stu-id="08116-127">Inquire</span></span>
- <span data-ttu-id="08116-128">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="08116-128">SilentlyContinue</span></span>
- <span data-ttu-id="08116-129">중지가</span><span class="sxs-lookup"><span data-stu-id="08116-129">Stop</span></span>
- <span data-ttu-id="08116-130">대기</span><span class="sxs-lookup"><span data-stu-id="08116-130">Suspend</span></span>

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

### <span data-ttu-id="08116-131">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="08116-131">-InformationVariable</span></span>
<span data-ttu-id="08116-132">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="08116-132">Specifies an information variable.</span></span>

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

### <span data-ttu-id="08116-133">-프로필</span><span class="sxs-lookup"><span data-stu-id="08116-133">-Profile</span></span>
<span data-ttu-id="08116-134">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="08116-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="08116-135">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="08116-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="08116-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08116-136">CommonParameters</span></span>
<span data-ttu-id="08116-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="08116-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08116-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08116-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08116-139">입력</span><span class="sxs-lookup"><span data-stu-id="08116-139">INPUTS</span></span>

## <span data-ttu-id="08116-140">출력</span><span class="sxs-lookup"><span data-stu-id="08116-140">OUTPUTS</span></span>

## <span data-ttu-id="08116-141">상속자</span><span class="sxs-lookup"><span data-stu-id="08116-141">NOTES</span></span>

## <span data-ttu-id="08116-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="08116-142">RELATED LINKS</span></span>

[<span data-ttu-id="08116-143">추가-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="08116-143">Add-AzureDisk</span></span>](./Add-AzureDisk.md)

[<span data-ttu-id="08116-144">-AzureDisk 제거</span><span class="sxs-lookup"><span data-stu-id="08116-144">Remove-AzureDisk</span></span>](./Remove-AzureDisk.md)

[<span data-ttu-id="08116-145">업데이트-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="08116-145">Update-AzureDisk</span></span>](./Update-AzureDisk.md)


