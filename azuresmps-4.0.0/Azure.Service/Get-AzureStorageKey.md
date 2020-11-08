---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 35588231-CBAC-4411-9531-9A06BD298ACA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7fdcad4b3a0f41f0589e49d4b33a767b93267855
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045548"
---
# <span data-ttu-id="635d0-101">Get-AzureStorageKey</span><span class="sxs-lookup"><span data-stu-id="635d0-101">Get-AzureStorageKey</span></span>

## <span data-ttu-id="635d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="635d0-102">SYNOPSIS</span></span>
<span data-ttu-id="635d0-103">Azure 저장소 계정에 대 한 기본 및 보조 저장소 계정 키를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="635d0-103">Returns the primary and secondary storage account keys for an Azure storage account.</span></span>

## <span data-ttu-id="635d0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="635d0-104">SYNTAX</span></span>

```
Get-AzureStorageKey [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="635d0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="635d0-105">DESCRIPTION</span></span>
<span data-ttu-id="635d0-106">**Get-AzureStorageKey** Cmdlet은 azure 저장소 계정 이름, 기본 계정 키, 지정 된 Azure 저장소 계정의 보조 계정 키를 포함 하는 개체를 속성으로 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="635d0-106">The **Get-AzureStorageKey** cmdlet returns an object with the Azure Storage account name, the primary account key, and the secondary account key of the specified Azure storage account as properties.</span></span>

## <span data-ttu-id="635d0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="635d0-107">EXAMPLES</span></span>

### <span data-ttu-id="635d0-108">예제 1: 기본 및 보조 저장소 키를 포함 하는 개체 가져오기</span><span class="sxs-lookup"><span data-stu-id="635d0-108">Example 1: Get an object that contains primary and secondary storage keys</span></span>
```
PS C:\> Get-AzureStorageKey -StorageAccountName "ContosoStore01"
```

<span data-ttu-id="635d0-109">이 명령은 ContosoStore01 저장소 계정에 대 한 기본 및 보조 저장소 키를 사용 하 여 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="635d0-109">This command gets an object with the primary and secondary storage keys for the ContosoStore01 storage account.</span></span>

### <span data-ttu-id="635d0-110">예제 2: 기본 저장소 계정 키를 받아 변수에 저장</span><span class="sxs-lookup"><span data-stu-id="635d0-110">Example 2: Get the primary storage account key and store it in a variable</span></span>
```
PS C:\> $ContosoStoreKey = (Get-AzureStorageKey -StorageAccountName "ContosoStore01").Primary
```

<span data-ttu-id="635d0-111">이 명령은 ContosoStore01 저장소 계정에 대 한 기본 저장소 계정 키를 $ContosoStoreKey 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="635d0-111">This command puts the primary storage account key for the ContosoStore01 storage account in the $ContosoStoreKey variable.</span></span>

## <span data-ttu-id="635d0-112">변수</span><span class="sxs-lookup"><span data-stu-id="635d0-112">PARAMETERS</span></span>

### <span data-ttu-id="635d0-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="635d0-113">-InformationAction</span></span>
<span data-ttu-id="635d0-114">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="635d0-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="635d0-115">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="635d0-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="635d0-116">하기로</span><span class="sxs-lookup"><span data-stu-id="635d0-116">Continue</span></span>
- <span data-ttu-id="635d0-117">숨기기</span><span class="sxs-lookup"><span data-stu-id="635d0-117">Ignore</span></span>
- <span data-ttu-id="635d0-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="635d0-118">Inquire</span></span>
- <span data-ttu-id="635d0-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="635d0-119">SilentlyContinue</span></span>
- <span data-ttu-id="635d0-120">중지가</span><span class="sxs-lookup"><span data-stu-id="635d0-120">Stop</span></span>
- <span data-ttu-id="635d0-121">대기</span><span class="sxs-lookup"><span data-stu-id="635d0-121">Suspend</span></span>

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

### <span data-ttu-id="635d0-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="635d0-122">-InformationVariable</span></span>
<span data-ttu-id="635d0-123">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="635d0-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="635d0-124">-프로필</span><span class="sxs-lookup"><span data-stu-id="635d0-124">-Profile</span></span>
<span data-ttu-id="635d0-125">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="635d0-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="635d0-126">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="635d0-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="635d0-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="635d0-127">-StorageAccountName</span></span>
<span data-ttu-id="635d0-128">저장소 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="635d0-128">Specifies the storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="635d0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="635d0-129">CommonParameters</span></span>
<span data-ttu-id="635d0-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="635d0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="635d0-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="635d0-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="635d0-132">입력</span><span class="sxs-lookup"><span data-stu-id="635d0-132">INPUTS</span></span>

## <span data-ttu-id="635d0-133">출력</span><span class="sxs-lookup"><span data-stu-id="635d0-133">OUTPUTS</span></span>

## <span data-ttu-id="635d0-134">상속자</span><span class="sxs-lookup"><span data-stu-id="635d0-134">NOTES</span></span>
* <span data-ttu-id="635d0-135">Node.js에 대 한 도움말을 보려면 `help node-dev` 명령을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="635d0-135">To get help with Node.js, use the `help node-dev` command.</span></span> <span data-ttu-id="635d0-136">PHP 확장에 대 한 도움말을 보려면이 `help php-dev` 명령을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="635d0-136">For help with PHP extensions, use the `help php-dev` command.</span></span>

## <span data-ttu-id="635d0-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="635d0-137">RELATED LINKS</span></span>

[<span data-ttu-id="635d0-138">Get-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="635d0-138">Get-AzureStorageAccount</span></span>](./Get-AzureStorageAccount.md)

[<span data-ttu-id="635d0-139">새-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="635d0-139">New-AzureStorageAccount</span></span>](./New-AzureStorageAccount.md)

[<span data-ttu-id="635d0-140">새-AzureStorageKey</span><span class="sxs-lookup"><span data-stu-id="635d0-140">New-AzureStorageKey</span></span>](./New-AzureStorageKey.md)

[<span data-ttu-id="635d0-141">-AzureStorageAccount 제거</span><span class="sxs-lookup"><span data-stu-id="635d0-141">Remove-AzureStorageAccount</span></span>](./Remove-AzureStorageAccount.md)

[<span data-ttu-id="635d0-142">Set-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="635d0-142">Set-AzureStorageAccount</span></span>](./Set-AzureStorageAccount.md)


