---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 849714BC-8B19-453E-B790-A9C38F9D48CB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8ef8bd3b1fef6a3af01193a104f6917c4131064f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045425"
---
# <span data-ttu-id="38177-101">Update-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="38177-101">Update-AzureDisk</span></span>

## <span data-ttu-id="38177-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38177-102">SYNOPSIS</span></span>
<span data-ttu-id="38177-103">Azure 디스크 리포지토리에서 디스크의 레이블을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="38177-103">Changes the label of a disk in the Azure disk repository.</span></span>

## <span data-ttu-id="38177-104">구문과</span><span class="sxs-lookup"><span data-stu-id="38177-104">SYNTAX</span></span>

### <span data-ttu-id="38177-105">길이</span><span class="sxs-lookup"><span data-stu-id="38177-105">Resize</span></span>
```
Update-AzureDisk [-DiskName] <String> [[-Label] <String>] [-ResizedSizeInGB] <Int32>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="38177-106">로이 Esize</span><span class="sxs-lookup"><span data-stu-id="38177-106">NoResize</span></span>
```
Update-AzureDisk [-DiskName] <String> [-Label] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="38177-107">설명은</span><span class="sxs-lookup"><span data-stu-id="38177-107">DESCRIPTION</span></span>
<span data-ttu-id="38177-108">**업데이트 azuredisk** cmdlet은 현재 Azure 구독의 디스크 리포지토리에서 디스크에 연결 된 레이블을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="38177-108">The **Update-AzureDisk** cmdlet changes the label that is associated with a disk in the disk repository of the current Azure subscription.</span></span>

## <span data-ttu-id="38177-109">예제의</span><span class="sxs-lookup"><span data-stu-id="38177-109">EXAMPLES</span></span>

### <span data-ttu-id="38177-110">예제 1: 디스크 레이블 변경</span><span class="sxs-lookup"><span data-stu-id="38177-110">Example 1: Change the label of a disk</span></span>
```
PS C:\> Update-AzureDisk ?DiskName "ContosoOSDisk" -Label "DoNotUse"
```

<span data-ttu-id="38177-111">이 명령은 ContosoOSDisk 이라는 이름의 디스크 레이블을 DoNotUse으로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="38177-111">This command changes the label of the disk named ContosoOSDisk to DoNotUse.</span></span>

## <span data-ttu-id="38177-112">변수</span><span class="sxs-lookup"><span data-stu-id="38177-112">PARAMETERS</span></span>

### <span data-ttu-id="38177-113">-DiskName</span><span class="sxs-lookup"><span data-stu-id="38177-113">-DiskName</span></span>
<span data-ttu-id="38177-114">이 cmdlet이 수정 하는 디스크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="38177-114">Specifies the name of the disk that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="38177-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="38177-115">-InformationAction</span></span>
<span data-ttu-id="38177-116">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="38177-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="38177-117">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="38177-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="38177-118">하기로</span><span class="sxs-lookup"><span data-stu-id="38177-118">Continue</span></span>
- <span data-ttu-id="38177-119">숨기기</span><span class="sxs-lookup"><span data-stu-id="38177-119">Ignore</span></span>
- <span data-ttu-id="38177-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="38177-120">Inquire</span></span>
- <span data-ttu-id="38177-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="38177-121">SilentlyContinue</span></span>
- <span data-ttu-id="38177-122">중지가</span><span class="sxs-lookup"><span data-stu-id="38177-122">Stop</span></span>
- <span data-ttu-id="38177-123">대기</span><span class="sxs-lookup"><span data-stu-id="38177-123">Suspend</span></span>

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

### <span data-ttu-id="38177-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="38177-124">-InformationVariable</span></span>
<span data-ttu-id="38177-125">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="38177-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="38177-126">-레이블</span><span class="sxs-lookup"><span data-stu-id="38177-126">-Label</span></span>
<span data-ttu-id="38177-127">디스크에 대 한 새 레이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="38177-127">Specifies the new label for the disk.</span></span>

```yaml
Type: String
Parameter Sets: Resize
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: NoResize
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38177-128">-프로필</span><span class="sxs-lookup"><span data-stu-id="38177-128">-Profile</span></span>
<span data-ttu-id="38177-129">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="38177-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="38177-130">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="38177-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="38177-131">-ResizedSizeInGB</span><span class="sxs-lookup"><span data-stu-id="38177-131">-ResizedSizeInGB</span></span>
<span data-ttu-id="38177-132">디스크의 새 크기 (기가바이트)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="38177-132">Specifies the new size, in gigabytes, for the disk.</span></span>

```yaml
Type: Int32
Parameter Sets: Resize
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38177-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38177-133">CommonParameters</span></span>
<span data-ttu-id="38177-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="38177-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38177-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38177-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38177-136">입력</span><span class="sxs-lookup"><span data-stu-id="38177-136">INPUTS</span></span>

## <span data-ttu-id="38177-137">출력</span><span class="sxs-lookup"><span data-stu-id="38177-137">OUTPUTS</span></span>

### <span data-ttu-id="38177-138">DiskContext</span><span class="sxs-lookup"><span data-stu-id="38177-138">DiskContext</span></span>

## <span data-ttu-id="38177-139">상속자</span><span class="sxs-lookup"><span data-stu-id="38177-139">NOTES</span></span>

## <span data-ttu-id="38177-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="38177-140">RELATED LINKS</span></span>

[<span data-ttu-id="38177-141">추가-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="38177-141">Add-AzureDisk</span></span>](./Add-AzureDisk.md)

[<span data-ttu-id="38177-142">Get-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="38177-142">Get-AzureDisk</span></span>](./Get-AzureDisk.md)

[<span data-ttu-id="38177-143">-AzureDisk 제거</span><span class="sxs-lookup"><span data-stu-id="38177-143">Remove-AzureDisk</span></span>](./Remove-AzureDisk.md)


