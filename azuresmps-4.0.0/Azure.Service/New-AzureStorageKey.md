---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 09ABE9E2-1080-4DEF-92DD-B8FF4C8B308C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9afdaafa57592239d0c24870e4459d650fac84c3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046203"
---
# <span data-ttu-id="2f939-101">New-AzureStorageKey</span><span class="sxs-lookup"><span data-stu-id="2f939-101">New-AzureStorageKey</span></span>

## <span data-ttu-id="2f939-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f939-102">SYNOPSIS</span></span>
<span data-ttu-id="2f939-103">Azure 저장소 계정의 저장소 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f939-103">Regenerates storage keys for an Azure storage account.</span></span>

## <span data-ttu-id="2f939-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2f939-104">SYNTAX</span></span>

```
New-AzureStorageKey [-KeyType] <String> [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="2f939-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2f939-105">DESCRIPTION</span></span>
<span data-ttu-id="2f939-106">**새-AzureStorageKey** Cmdlet은 Azure 저장소 계정에 대 한 기본 또는 보조 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f939-106">The **New-AzureStorageKey** cmdlet regenerates the primary or secondary key for an Azure Storage account.</span></span>
<span data-ttu-id="2f939-107">저장소 계정 이름, 기본 키 및 보조 키를 속성으로 포함 하는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f939-107">It returns an object that contains the storage account name, primary key, and secondary key as properties.</span></span>

## <span data-ttu-id="2f939-108">예제의</span><span class="sxs-lookup"><span data-stu-id="2f939-108">EXAMPLES</span></span>

### <span data-ttu-id="2f939-109">예제 1: 기본 저장소 키 다시 생성</span><span class="sxs-lookup"><span data-stu-id="2f939-109">Example 1: Regenerate a primary storage key</span></span>
```
PS C:\> New-AzureStorageKey -KeyType "Primary" -StorageAccountName "ContosoStore01"
```

<span data-ttu-id="2f939-110">이 명령은 ContosoStore01 저장소 계정에 대 한 기본 저장소 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f939-110">This command regenerates the primary storage key for the ContosoStore01 storage account.</span></span>

### <span data-ttu-id="2f939-111">예제 2: 보조 저장소 키를 다시 생성 하 고 변수에 저장</span><span class="sxs-lookup"><span data-stu-id="2f939-111">Example 2: Regenerate a secondary storage key and save it in a variable</span></span>
```
PS C:\> $ContosoStoreKey = New-AzureStorageKey -KeyType "Secondary" -StorageAccountName "ContosoStore01"
```

<span data-ttu-id="2f939-112">이 명령은 ContosoStore01 저장소 계정에 대 한 보조 저장소 키를 다시 생성 하 고 업데이트 된 저장소 계정 키 정보를 $ContosoStoreKey에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f939-112">This command regenerate the secondary storage key for the ContosoStore01 storage account and stores the updated storage account key information in the $ContosoStoreKey.</span></span>

## <span data-ttu-id="2f939-113">변수</span><span class="sxs-lookup"><span data-stu-id="2f939-113">PARAMETERS</span></span>

### <span data-ttu-id="2f939-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="2f939-114">-InformationAction</span></span>
<span data-ttu-id="2f939-115">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f939-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="2f939-116">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2f939-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2f939-117">하기로</span><span class="sxs-lookup"><span data-stu-id="2f939-117">Continue</span></span>
- <span data-ttu-id="2f939-118">숨기기</span><span class="sxs-lookup"><span data-stu-id="2f939-118">Ignore</span></span>
- <span data-ttu-id="2f939-119">Inquire</span><span class="sxs-lookup"><span data-stu-id="2f939-119">Inquire</span></span>
- <span data-ttu-id="2f939-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="2f939-120">SilentlyContinue</span></span>
- <span data-ttu-id="2f939-121">중지가</span><span class="sxs-lookup"><span data-stu-id="2f939-121">Stop</span></span>
- <span data-ttu-id="2f939-122">대기</span><span class="sxs-lookup"><span data-stu-id="2f939-122">Suspend</span></span>

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

### <span data-ttu-id="2f939-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="2f939-123">-InformationVariable</span></span>
<span data-ttu-id="2f939-124">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f939-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="2f939-125">-KeyType</span><span class="sxs-lookup"><span data-stu-id="2f939-125">-KeyType</span></span>
<span data-ttu-id="2f939-126">재생성할 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f939-126">Specifies which key to regenerate.</span></span>
<span data-ttu-id="2f939-127">유효한 값은 Primary 및 Secondary입니다.</span><span class="sxs-lookup"><span data-stu-id="2f939-127">Valid values are: Primary and Secondary.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f939-128">-프로필</span><span class="sxs-lookup"><span data-stu-id="2f939-128">-Profile</span></span>
<span data-ttu-id="2f939-129">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f939-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2f939-130">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="2f939-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2f939-131">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="2f939-131">-StorageAccountName</span></span>
<span data-ttu-id="2f939-132">키를 다시 생성할 Azure Storage 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f939-132">Specifies the name of the Azure Storage account for which to regenerate a key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f939-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f939-133">CommonParameters</span></span>
<span data-ttu-id="2f939-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f939-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f939-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f939-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f939-136">입력</span><span class="sxs-lookup"><span data-stu-id="2f939-136">INPUTS</span></span>

## <span data-ttu-id="2f939-137">출력</span><span class="sxs-lookup"><span data-stu-id="2f939-137">OUTPUTS</span></span>

### <span data-ttu-id="2f939-138">StorageServiceKeys</span><span class="sxs-lookup"><span data-stu-id="2f939-138">StorageServiceKeys</span></span>

## <span data-ttu-id="2f939-139">상속자</span><span class="sxs-lookup"><span data-stu-id="2f939-139">NOTES</span></span>

## <span data-ttu-id="2f939-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2f939-140">RELATED LINKS</span></span>

[<span data-ttu-id="2f939-141">Get-AzureStorageKey</span><span class="sxs-lookup"><span data-stu-id="2f939-141">Get-AzureStorageKey</span></span>](./Get-AzureStorageKey.md)


