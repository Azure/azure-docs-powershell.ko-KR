---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BF5526C1-11B9-47A8-A5A6-CB275B470A9E
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8c22b3eb95ab940670043f9ae467663c951027d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523992"
---
# <span data-ttu-id="b0782-101">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b0782-101">Get-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="b0782-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0782-102">SYNOPSIS</span></span>
<span data-ttu-id="b0782-103">Azure storage 테이블에 대 한 저장 된 액세스 정책 또는 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b0782-103">Gets the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="b0782-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b0782-104">SYNTAX</span></span>

```
Get-AzureStorageTableStoredAccessPolicy [-Table] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="b0782-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b0782-105">DESCRIPTION</span></span>
<span data-ttu-id="b0782-106">**AzureStorageTableStoredAccessPolicy** Cmdlet은 Azure storage 테이블에 대 한 저장 된 액세스 정책 또는 정책을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0782-106">The **Get-AzureStorageTableStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="b0782-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b0782-107">EXAMPLES</span></span>

### <span data-ttu-id="b0782-108">예제 1: 저장소 테이블에 저장 된 액세스 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="b0782-108">Example 1: Get a stored access policy in a storage table</span></span>
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02" -Policy "Policy50"
```

<span data-ttu-id="b0782-109">이 명령은 Table02 이라는 저장소 테이블에서 Policy50 라는 액세스 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b0782-109">This command gets the access policy named Policy50 in the storage table named Table02.</span></span>

### <span data-ttu-id="b0782-110">예제 2: 저장소 테이블에 저장 된 모든 액세스 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="b0782-110">Example 2: Get all stored access policies in a storage table</span></span>
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02"
```

<span data-ttu-id="b0782-111">이 명령은 Table02 이라는 테이블에 있는 모든 액세스 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b0782-111">This command gets all access policies in the table named Table02.</span></span>

## <span data-ttu-id="b0782-112">변수</span><span class="sxs-lookup"><span data-stu-id="b0782-112">PARAMETERS</span></span>

### <span data-ttu-id="b0782-113">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="b0782-113">-Context</span></span>
<span data-ttu-id="b0782-114">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0782-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="b0782-115">저장소 컨텍스트를 얻으려면 New-AzureStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0782-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0782-116">-정책</span><span class="sxs-lookup"><span data-stu-id="b0782-116">-Policy</span></span>
<span data-ttu-id="b0782-117">이 SA (공유 액세스 서명) 토큰에 대 한 사용 권한을 포함 하는 저장 된 액세스 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0782-117">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0782-118">-테이블</span><span class="sxs-lookup"><span data-stu-id="b0782-118">-Table</span></span>
<span data-ttu-id="b0782-119">Azure 저장소 테이블 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0782-119">Specifies the Azure storage table name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0782-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0782-120">CommonParameters</span></span>
<span data-ttu-id="b0782-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0782-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0782-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0782-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0782-123">입력</span><span class="sxs-lookup"><span data-stu-id="b0782-123">INPUTS</span></span>

## <span data-ttu-id="b0782-124">출력</span><span class="sxs-lookup"><span data-stu-id="b0782-124">OUTPUTS</span></span>

## <span data-ttu-id="b0782-125">상속자</span><span class="sxs-lookup"><span data-stu-id="b0782-125">NOTES</span></span>

## <span data-ttu-id="b0782-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b0782-126">RELATED LINKS</span></span>

[<span data-ttu-id="b0782-127">새로운 AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b0782-127">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="b0782-128">제거-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b0782-128">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="b0782-129">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b0782-129">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="b0782-130">새로운 AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="b0782-130">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


