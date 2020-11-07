---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BF5526C1-11B9-47A8-A5A6-CB275B470A9E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTableStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 85501affef70ce0cf31e62f9083d5ed383425497
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702081"
---
# <span data-ttu-id="5e726-101">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5e726-101">Get-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="5e726-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e726-102">SYNOPSIS</span></span>
<span data-ttu-id="5e726-103">Azure storage 테이블에 대 한 저장 된 액세스 정책 또는 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5e726-103">Gets the stored access policy or policies for an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e726-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5e726-104">SYNTAX</span></span>

```
Get-AzureStorageTableStoredAccessPolicy [-Table] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="5e726-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5e726-105">DESCRIPTION</span></span>
<span data-ttu-id="5e726-106">**AzureStorageTableStoredAccessPolicy** Cmdlet은 Azure storage 테이블에 대 한 저장 된 액세스 정책 또는 정책을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e726-106">The **Get-AzureStorageTableStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="5e726-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5e726-107">EXAMPLES</span></span>

### <span data-ttu-id="5e726-108">예제 1: 저장소 테이블에 저장 된 액세스 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="5e726-108">Example 1: Get a stored access policy in a storage table</span></span>
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02" -Policy "Policy50"
```

<span data-ttu-id="5e726-109">이 명령은 Table02 이라는 저장소 테이블에서 Policy50 라는 액세스 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5e726-109">This command gets the access policy named Policy50 in the storage table named Table02.</span></span>

### <span data-ttu-id="5e726-110">예제 2: 저장소 테이블에 저장 된 모든 액세스 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="5e726-110">Example 2: Get all stored access policies in a storage table</span></span>
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02"
```

<span data-ttu-id="5e726-111">이 명령은 Table02 이라는 테이블에 있는 모든 액세스 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5e726-111">This command gets all access policies in the table named Table02.</span></span>

## <span data-ttu-id="5e726-112">변수</span><span class="sxs-lookup"><span data-stu-id="5e726-112">PARAMETERS</span></span>

### <span data-ttu-id="5e726-113">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="5e726-113">-Context</span></span>
<span data-ttu-id="5e726-114">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e726-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="5e726-115">저장소 컨텍스트를 얻으려면 New-AzureStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e726-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="5e726-116">-정책</span><span class="sxs-lookup"><span data-stu-id="5e726-116">-Policy</span></span>
<span data-ttu-id="5e726-117">이 SA (공유 액세스 서명) 토큰에 대 한 사용 권한을 포함 하는 저장 된 액세스 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e726-117">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="5e726-118">-테이블</span><span class="sxs-lookup"><span data-stu-id="5e726-118">-Table</span></span>
<span data-ttu-id="5e726-119">Azure 저장소 테이블 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e726-119">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="5e726-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e726-120">CommonParameters</span></span>
<span data-ttu-id="5e726-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e726-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e726-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e726-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e726-123">입력</span><span class="sxs-lookup"><span data-stu-id="5e726-123">INPUTS</span></span>

### <span data-ttu-id="5e726-124">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="5e726-124">IStorageContext</span></span>

<span data-ttu-id="5e726-125">' Context ' 매개 변수는 파이프라인에서 ' IStorageContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e726-125">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="5e726-126">이름</span><span class="sxs-lookup"><span data-stu-id="5e726-126">String</span></span>

<span data-ttu-id="5e726-127">' Table ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e726-127">Parameter 'Table' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="5e726-128">출력</span><span class="sxs-lookup"><span data-stu-id="5e726-128">OUTPUTS</span></span>

### <span data-ttu-id="5e726-129">WindowsAzure. SharedAccessTablePolicy</span><span class="sxs-lookup"><span data-stu-id="5e726-129">Microsoft.WindowsAzure.Storage.Table.SharedAccessTablePolicy</span></span>

## <span data-ttu-id="5e726-130">상속자</span><span class="sxs-lookup"><span data-stu-id="5e726-130">NOTES</span></span>

## <span data-ttu-id="5e726-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5e726-131">RELATED LINKS</span></span>

[<span data-ttu-id="5e726-132">새로운 AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5e726-132">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="5e726-133">제거-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5e726-133">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="5e726-134">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5e726-134">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="5e726-135">새로운 AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="5e726-135">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


