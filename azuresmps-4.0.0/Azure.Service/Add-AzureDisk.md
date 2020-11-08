---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 16A34F31-1C61-4911-8C1F-9F82683524A1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 775d2deff8a83e758d48fb9328bf4156b142d20c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046393"
---
# <span data-ttu-id="16eb3-101">Add-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="16eb3-101">Add-AzureDisk</span></span>

## <span data-ttu-id="16eb3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16eb3-102">SYNOPSIS</span></span>
<span data-ttu-id="16eb3-103">디스크를 Azure 디스크 리포지토리에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="16eb3-103">Adds a disk to the Azure disk repository.</span></span>

## <span data-ttu-id="16eb3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="16eb3-104">SYNTAX</span></span>

```
Add-AzureDisk [-DiskName] <String> [-MediaLocation] <String> [-Label <String>] [-OS <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="16eb3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="16eb3-105">DESCRIPTION</span></span>
<span data-ttu-id="16eb3-106">**추가-AzureDisk** cmdlet는 현재 구독의 Azure 디스크 리포지토리에 디스크를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="16eb3-106">The **Add-AzureDisk** cmdlet adds a disk to the Azure disk repository in the current subscription.</span></span>
<span data-ttu-id="16eb3-107">이 cmdlet은 시스템 디스크 또는 데이터 디스크를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16eb3-107">This cmdlet can add a system disk or a data disk.</span></span>
<span data-ttu-id="16eb3-108">시스템 디스크를 추가 하려면 *OS* 매개 변수를 사용 하 여 운영 체제 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16eb3-108">To add a system disk, specify an operating system type by using the *OS* parameter.</span></span>

## <span data-ttu-id="16eb3-109">예제의</span><span class="sxs-lookup"><span data-stu-id="16eb3-109">EXAMPLES</span></span>

### <span data-ttu-id="16eb3-110">예제 1: Windows 운영 체제를 사용 하는 시동 디스크 추가</span><span class="sxs-lookup"><span data-stu-id="16eb3-110">Example 1: Add a startup disk that uses the Windows operating system</span></span>
```
PS C:\> Add-AzureDisk -DiskName "MyWinDisk" -MediaLocation "http://contosostorage.blob.core.azure.com/vhds/winserver-system.vhd" -Label "StartupDisk" -OS "Windows"
```

<span data-ttu-id="16eb3-111">이 명령은 디스크 리포지토리에 시스템 디스크를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="16eb3-111">This command adds a system disk to your disk repository.</span></span>
<span data-ttu-id="16eb3-112">시스템 디스크는 Windows 운영 체제를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="16eb3-112">The system disk uses the Windows operating system.</span></span>

### <span data-ttu-id="16eb3-113">예제 2: 데이터 디스크 추가</span><span class="sxs-lookup"><span data-stu-id="16eb3-113">Example 2: Add a data disk</span></span>
```
PS C:\> Add-AzureDisk -DiskName "MyDataDisk" -MediaLocation "http://yourstorageaccount.blob.core.azure.com/vhds/winserver-data.vhd" -Label "DataDisk"
```

<span data-ttu-id="16eb3-114">이 명령은 데이터 디스크를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="16eb3-114">This command adds a data disk.</span></span>

### <span data-ttu-id="16eb3-115">예제 3: Linux 시스템 디스크 추가</span><span class="sxs-lookup"><span data-stu-id="16eb3-115">Example 3: Add a Linux system disk</span></span>
```
PS C:\> Add-AzureDisk -DiskName "MyLinuxDisk" -MediaLocation "http://yourstorageaccount.blob.core.azure.com/vhds/linuxsys.vhd" -OS "Linux"
```

<span data-ttu-id="16eb3-116">이 명령은 Linux 시스템 디스크를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="16eb3-116">This command adds a Linux system disk.</span></span>

## <span data-ttu-id="16eb3-117">변수</span><span class="sxs-lookup"><span data-stu-id="16eb3-117">PARAMETERS</span></span>

### <span data-ttu-id="16eb3-118">-DiskName</span><span class="sxs-lookup"><span data-stu-id="16eb3-118">-DiskName</span></span>
<span data-ttu-id="16eb3-119">이 cmdlet이 추가 하는 디스크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16eb3-119">Specifies the name of the disk that this cmdlet adds.</span></span>

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

### <span data-ttu-id="16eb3-120">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="16eb3-120">-InformationAction</span></span>
<span data-ttu-id="16eb3-121">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16eb3-121">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="16eb3-122">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="16eb3-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="16eb3-123">하기로</span><span class="sxs-lookup"><span data-stu-id="16eb3-123">Continue</span></span>
- <span data-ttu-id="16eb3-124">숨기기</span><span class="sxs-lookup"><span data-stu-id="16eb3-124">Ignore</span></span>
- <span data-ttu-id="16eb3-125">Inquire</span><span class="sxs-lookup"><span data-stu-id="16eb3-125">Inquire</span></span>
- <span data-ttu-id="16eb3-126">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="16eb3-126">SilentlyContinue</span></span>
- <span data-ttu-id="16eb3-127">중지가</span><span class="sxs-lookup"><span data-stu-id="16eb3-127">Stop</span></span>
- <span data-ttu-id="16eb3-128">대기</span><span class="sxs-lookup"><span data-stu-id="16eb3-128">Suspend</span></span>

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

### <span data-ttu-id="16eb3-129">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="16eb3-129">-InformationVariable</span></span>
<span data-ttu-id="16eb3-130">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16eb3-130">Specifies an information variable.</span></span>

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

### <span data-ttu-id="16eb3-131">-레이블</span><span class="sxs-lookup"><span data-stu-id="16eb3-131">-Label</span></span>
<span data-ttu-id="16eb3-132">이 cmdlet이 추가 하는 디스크에 대 한 디스크 레이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16eb3-132">Specifies a disk label for the disk that this cmdlet adds.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16eb3-133">-MediaLocation</span><span class="sxs-lookup"><span data-stu-id="16eb3-133">-MediaLocation</span></span>
<span data-ttu-id="16eb3-134">Azure Storage에서 디스크의 실제 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16eb3-134">Specifies the physical location of the disk in Azure Storage.</span></span>
<span data-ttu-id="16eb3-135">이 값은 현재 구독 및 저장소 계정의 blob 페이지를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="16eb3-135">This value refers to a blob page in the current subscription and storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16eb3-136">-OS</span><span class="sxs-lookup"><span data-stu-id="16eb3-136">-OS</span></span>
<span data-ttu-id="16eb3-137">시스템 디스크의 운영 체제 종류를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16eb3-137">Specifies the operating system type for a system disk.</span></span>
<span data-ttu-id="16eb3-138">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="16eb3-138">Valid values are:</span></span> 

- <span data-ttu-id="16eb3-139">창을</span><span class="sxs-lookup"><span data-stu-id="16eb3-139">Windows</span></span> 
- <span data-ttu-id="16eb3-140">Linux</span><span class="sxs-lookup"><span data-stu-id="16eb3-140">Linux</span></span> 

<span data-ttu-id="16eb3-141">이 매개 변수를 지정 하지 않으면 cmdlet이 디스크를 데이터 디스크로 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="16eb3-141">If you do not specify this parameter, the cmdlet adds the disk as a data disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16eb3-142">-프로필</span><span class="sxs-lookup"><span data-stu-id="16eb3-142">-Profile</span></span>
<span data-ttu-id="16eb3-143">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16eb3-143">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="16eb3-144">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="16eb3-144">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="16eb3-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16eb3-145">CommonParameters</span></span>
<span data-ttu-id="16eb3-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="16eb3-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16eb3-147">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16eb3-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16eb3-148">입력</span><span class="sxs-lookup"><span data-stu-id="16eb3-148">INPUTS</span></span>

## <span data-ttu-id="16eb3-149">출력</span><span class="sxs-lookup"><span data-stu-id="16eb3-149">OUTPUTS</span></span>

### <span data-ttu-id="16eb3-150">DiskContext</span><span class="sxs-lookup"><span data-stu-id="16eb3-150">DiskContext</span></span>

## <span data-ttu-id="16eb3-151">상속자</span><span class="sxs-lookup"><span data-stu-id="16eb3-151">NOTES</span></span>

## <span data-ttu-id="16eb3-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="16eb3-152">RELATED LINKS</span></span>

[<span data-ttu-id="16eb3-153">Get-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="16eb3-153">Get-AzureDisk</span></span>](./Get-AzureDisk.md)

[<span data-ttu-id="16eb3-154">-AzureDisk 제거</span><span class="sxs-lookup"><span data-stu-id="16eb3-154">Remove-AzureDisk</span></span>](./Remove-AzureDisk.md)

[<span data-ttu-id="16eb3-155">업데이트-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="16eb3-155">Update-AzureDisk</span></span>](./Update-AzureDisk.md)


