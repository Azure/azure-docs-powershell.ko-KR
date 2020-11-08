---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7D7D1FAE-5360-428B-AAE9-9D1109A7B67F
online version: ''
schema: 2.0.0
ms.openlocfilehash: faccd241929beca1f2423fa9c23f35793233205b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045549"
---
# <span data-ttu-id="951ce-101">Get-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="951ce-101">Get-AzureStorageAccount</span></span>

## <span data-ttu-id="951ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="951ce-102">SYNOPSIS</span></span>
<span data-ttu-id="951ce-103">현재 Azure 구독에 대 한 저장소 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="951ce-103">Gets the storage accounts for the current Azure subscription.</span></span>

## <span data-ttu-id="951ce-104">구문과</span><span class="sxs-lookup"><span data-stu-id="951ce-104">SYNTAX</span></span>

```
Get-AzureStorageAccount [[-StorageAccountName] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="951ce-105">설명은</span><span class="sxs-lookup"><span data-stu-id="951ce-105">DESCRIPTION</span></span>
<span data-ttu-id="951ce-106">**Get-AzureStorageAccount** cmdlet은 현재 구독의 저장소 계정에 대 한 정보를 포함 하는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="951ce-106">The **Get-AzureStorageAccount** cmdlet returns an object containing information about the storage accounts for the current subscription.</span></span>
<span data-ttu-id="951ce-107">*Storageaccountname* 매개 변수를 지정 하면 지정 된 저장소 계정에 대 한 정보만 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="951ce-107">If the *StorageAccountName* parameter is specified, then only information about the specified storage account is returned.</span></span>

## <span data-ttu-id="951ce-108">예제의</span><span class="sxs-lookup"><span data-stu-id="951ce-108">EXAMPLES</span></span>

### <span data-ttu-id="951ce-109">예제 1: 모든 저장소 계정 반환</span><span class="sxs-lookup"><span data-stu-id="951ce-109">Example 1: Return all storage accounts</span></span>
```
PS C:\> Get-AzureStorageAccount
```

<span data-ttu-id="951ce-110">이 명령은 현재 구독과 연결 된 모든 저장소 계정이 포함 된 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="951ce-110">This command returns an object with all the storage accounts associated with the current subscription.</span></span>

### <span data-ttu-id="951ce-111">예제 2: 지정 된 계정에 대 한 계정 정보 반환</span><span class="sxs-lookup"><span data-stu-id="951ce-111">Example 2: Return account information for a specified account</span></span>
```
PS C:\> Get-AzureStorageAccount -StorageAccountName "ContosoStore01"
```

<span data-ttu-id="951ce-112">이 명령은 ContosoStore01 계정 정보만 포함 하는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="951ce-112">This command returns an object with only the ContosoStore01 account information.</span></span>

### <span data-ttu-id="951ce-113">예제 3: 저장소 계정 테이블 표시</span><span class="sxs-lookup"><span data-stu-id="951ce-113">Example 3: Display a table of storage accounts</span></span>
```
PS C:\> Get-AzureStorageAccount | Format-Table -AutoSize -Property @{Label="Name";Expression={$_.StorageAccountName}},"Label","Location"
```

<span data-ttu-id="951ce-114">이 명령은 현재 구독과 연결 된 모든 저장소 계정이 포함 된 개체를 반환 하 고, 계정 이름, 계정 레이블, 저장소 위치를 나타내는 테이블로 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="951ce-114">This command returns an object with all the storage accounts associated with the current subscription, and outputs them as a table showing the account name, the account label, and the storage location.</span></span>

## <span data-ttu-id="951ce-115">변수</span><span class="sxs-lookup"><span data-stu-id="951ce-115">PARAMETERS</span></span>

### <span data-ttu-id="951ce-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="951ce-116">-InformationAction</span></span>
<span data-ttu-id="951ce-117">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="951ce-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="951ce-118">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="951ce-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="951ce-119">하기로</span><span class="sxs-lookup"><span data-stu-id="951ce-119">Continue</span></span>
- <span data-ttu-id="951ce-120">숨기기</span><span class="sxs-lookup"><span data-stu-id="951ce-120">Ignore</span></span>
- <span data-ttu-id="951ce-121">Inquire</span><span class="sxs-lookup"><span data-stu-id="951ce-121">Inquire</span></span>
- <span data-ttu-id="951ce-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="951ce-122">SilentlyContinue</span></span>
- <span data-ttu-id="951ce-123">중지가</span><span class="sxs-lookup"><span data-stu-id="951ce-123">Stop</span></span>
- <span data-ttu-id="951ce-124">대기</span><span class="sxs-lookup"><span data-stu-id="951ce-124">Suspend</span></span>

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

### <span data-ttu-id="951ce-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="951ce-125">-InformationVariable</span></span>
<span data-ttu-id="951ce-126">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="951ce-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="951ce-127">-프로필</span><span class="sxs-lookup"><span data-stu-id="951ce-127">-Profile</span></span>
<span data-ttu-id="951ce-128">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="951ce-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="951ce-129">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="951ce-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="951ce-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="951ce-130">-StorageAccountName</span></span>
<span data-ttu-id="951ce-131">저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="951ce-131">Specifies the name of a storage account.</span></span>
<span data-ttu-id="951ce-132">지정 된 경우이 cmdlet은 지정 된 저장소 계정 개체만 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="951ce-132">If specified, this cmdlet returns only the specified storage account object.</span></span>

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

### <span data-ttu-id="951ce-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="951ce-133">CommonParameters</span></span>
<span data-ttu-id="951ce-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="951ce-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="951ce-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="951ce-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="951ce-136">입력</span><span class="sxs-lookup"><span data-stu-id="951ce-136">INPUTS</span></span>

## <span data-ttu-id="951ce-137">출력</span><span class="sxs-lookup"><span data-stu-id="951ce-137">OUTPUTS</span></span>

### <span data-ttu-id="951ce-138">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="951ce-138">ManagementOperationContext</span></span>

## <span data-ttu-id="951ce-139">상속자</span><span class="sxs-lookup"><span data-stu-id="951ce-139">NOTES</span></span>
* <span data-ttu-id="951ce-140">`help node-dev`Node.js 개발 관련 cmdlet에 대 한 도움말을 보려면 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="951ce-140">Type `help node-dev` to get help on Node.js development-related cmdlets.</span></span> <span data-ttu-id="951ce-141">`help php-dev`PHP 개발 관련 cmdlet에 대 한 도움말을 보려면 입력 하세요.</span><span class="sxs-lookup"><span data-stu-id="951ce-141">Type `help php-dev` to get help on PHP development-related cmdlets.</span></span>

## <span data-ttu-id="951ce-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="951ce-142">RELATED LINKS</span></span>

[<span data-ttu-id="951ce-143">새-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="951ce-143">New-AzureStorageAccount</span></span>](./New-AzureStorageAccount.md)

[<span data-ttu-id="951ce-144">Set-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="951ce-144">Set-AzureStorageAccount</span></span>](./Set-AzureStorageAccount.md)


