---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 679452A6-A6CA-4DC8-8E00-09E369505319
online version: ''
schema: 2.0.0
ms.openlocfilehash: 933c6de8e7baa55b2093a7ffc4ac28fede13bb5b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046458"
---
# <span data-ttu-id="48fc6-101">Remove-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="48fc6-101">Remove-AzureStorageAccount</span></span>

## <span data-ttu-id="48fc6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48fc6-102">SYNOPSIS</span></span>
<span data-ttu-id="48fc6-103">지정 된 저장소 계정을 구독에서 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="48fc6-103">Deletes the specified storage account from a subscription.</span></span>

## <span data-ttu-id="48fc6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="48fc6-104">SYNTAX</span></span>

```
Remove-AzureStorageAccount [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="48fc6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="48fc6-105">DESCRIPTION</span></span>
<span data-ttu-id="48fc6-106">**제거-AzureStorageAccount** Cmdlet은 Azure 구독에서 계정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="48fc6-106">The **Remove-AzureStorageAccount** cmdlet removes an account from an Azure subscription.</span></span>

## <span data-ttu-id="48fc6-107">예제의</span><span class="sxs-lookup"><span data-stu-id="48fc6-107">EXAMPLES</span></span>

### <span data-ttu-id="48fc6-108">예제 1: 저장소 계정 제거</span><span class="sxs-lookup"><span data-stu-id="48fc6-108">Example 1: Remove a storage account</span></span>
```
PS C:\> Remove-AzureStorageAccount -StorageAccountName "ContosoStore01"
```

<span data-ttu-id="48fc6-109">이 명령은 지정 된 구독에서 ContosoStore01 저장소 계정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="48fc6-109">This command removes the ContosoStore01 storage account from the specified subscription.</span></span>

## <span data-ttu-id="48fc6-110">변수</span><span class="sxs-lookup"><span data-stu-id="48fc6-110">PARAMETERS</span></span>

### <span data-ttu-id="48fc6-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="48fc6-111">-InformationAction</span></span>
<span data-ttu-id="48fc6-112">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="48fc6-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="48fc6-113">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="48fc6-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="48fc6-114">하기로</span><span class="sxs-lookup"><span data-stu-id="48fc6-114">Continue</span></span>
- <span data-ttu-id="48fc6-115">숨기기</span><span class="sxs-lookup"><span data-stu-id="48fc6-115">Ignore</span></span>
- <span data-ttu-id="48fc6-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="48fc6-116">Inquire</span></span>
- <span data-ttu-id="48fc6-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="48fc6-117">SilentlyContinue</span></span>
- <span data-ttu-id="48fc6-118">중지가</span><span class="sxs-lookup"><span data-stu-id="48fc6-118">Stop</span></span>
- <span data-ttu-id="48fc6-119">대기</span><span class="sxs-lookup"><span data-stu-id="48fc6-119">Suspend</span></span>

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

### <span data-ttu-id="48fc6-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="48fc6-120">-InformationVariable</span></span>
<span data-ttu-id="48fc6-121">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="48fc6-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="48fc6-122">-프로필</span><span class="sxs-lookup"><span data-stu-id="48fc6-122">-Profile</span></span>
<span data-ttu-id="48fc6-123">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="48fc6-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="48fc6-124">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="48fc6-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="48fc6-125">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="48fc6-125">-StorageAccountName</span></span>
<span data-ttu-id="48fc6-126">제거할 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="48fc6-126">Specifies the name of the storage account to remove.</span></span>

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

### <span data-ttu-id="48fc6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48fc6-127">CommonParameters</span></span>
<span data-ttu-id="48fc6-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="48fc6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48fc6-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48fc6-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48fc6-130">입력</span><span class="sxs-lookup"><span data-stu-id="48fc6-130">INPUTS</span></span>

## <span data-ttu-id="48fc6-131">출력</span><span class="sxs-lookup"><span data-stu-id="48fc6-131">OUTPUTS</span></span>

## <span data-ttu-id="48fc6-132">상속자</span><span class="sxs-lookup"><span data-stu-id="48fc6-132">NOTES</span></span>

## <span data-ttu-id="48fc6-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="48fc6-133">RELATED LINKS</span></span>

[<span data-ttu-id="48fc6-134">Get-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="48fc6-134">Get-AzureStorageAccount</span></span>](./Get-AzureStorageAccount.md)

[<span data-ttu-id="48fc6-135">새-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="48fc6-135">New-AzureStorageAccount</span></span>](./New-AzureStorageAccount.md)

[<span data-ttu-id="48fc6-136">Set-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="48fc6-136">Set-AzureStorageAccount</span></span>](./Set-AzureStorageAccount.md)


