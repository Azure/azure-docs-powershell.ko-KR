---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: CF3B6E3B-3FC1-4871-AFE0-366B17A9E4F8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTableStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: b87dd24c78b835e16ab1c4e8e9c0c3bb265d4feb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537935"
---
# <span data-ttu-id="49f2a-101">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="49f2a-101">New-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="49f2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49f2a-102">SYNOPSIS</span></span>
<span data-ttu-id="49f2a-103">Azure storage 테이블에 대 한 저장 된 액세스 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="49f2a-103">Creates a stored access policy for an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49f2a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="49f2a-104">SYNTAX</span></span>

```
New-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="49f2a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="49f2a-105">DESCRIPTION</span></span>
<span data-ttu-id="49f2a-106">**AzureStorageTableStoredAccessPolicy** Cmdlet은 Azure storage 테이블에 대해 저장 된 액세스 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="49f2a-106">The **New-AzureStorageTableStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="49f2a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="49f2a-107">EXAMPLES</span></span>

### <span data-ttu-id="49f2a-108">예제 1: 테이블에 저장 된 액세스 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="49f2a-108">Example 1: Create a stored access policy in a table</span></span>
```
PS C:\>New-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy02"
```

<span data-ttu-id="49f2a-109">이 명령은 MyTable 이라는 저장소 테이블에 Policy02 라는 액세스 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="49f2a-109">This command creates an access policy named Policy02 in the storage table named MyTable.</span></span>

## <span data-ttu-id="49f2a-110">변수</span><span class="sxs-lookup"><span data-stu-id="49f2a-110">PARAMETERS</span></span>

### <span data-ttu-id="49f2a-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="49f2a-111">-Context</span></span>
<span data-ttu-id="49f2a-112">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="49f2a-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="49f2a-113">저장소 컨텍스트를 얻으려면 New-AzureStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="49f2a-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="49f2a-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="49f2a-114">-ExpiryTime</span></span>
<span data-ttu-id="49f2a-115">저장 된 액세스 정책이 무효화 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="49f2a-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49f2a-116">-사용 권한</span><span class="sxs-lookup"><span data-stu-id="49f2a-116">-Permission</span></span>
<span data-ttu-id="49f2a-117">저장 된 액세스 정책에서 저장소 테이블에 액세스 하는 데 필요한 권한을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="49f2a-117">Specifies permissions in the stored access policy to access the storage table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49f2a-118">-정책</span><span class="sxs-lookup"><span data-stu-id="49f2a-118">-Policy</span></span>
<span data-ttu-id="49f2a-119">저장 된 액세스 정책의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="49f2a-119">Specifies a name for the stored access policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49f2a-120">-StartTime</span><span class="sxs-lookup"><span data-stu-id="49f2a-120">-StartTime</span></span>
<span data-ttu-id="49f2a-121">저장 된 액세스 정책이 유효 하 게 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="49f2a-121">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49f2a-122">-테이블</span><span class="sxs-lookup"><span data-stu-id="49f2a-122">-Table</span></span>
<span data-ttu-id="49f2a-123">Azure 저장소 테이블 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="49f2a-123">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="49f2a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49f2a-124">CommonParameters</span></span>
<span data-ttu-id="49f2a-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="49f2a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49f2a-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49f2a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49f2a-127">입력</span><span class="sxs-lookup"><span data-stu-id="49f2a-127">INPUTS</span></span>

### <span data-ttu-id="49f2a-128">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="49f2a-128">IStorageContext</span></span>

<span data-ttu-id="49f2a-129">' Context ' 매개 변수는 파이프라인에서 ' IStorageContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="49f2a-129">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="49f2a-130">이름</span><span class="sxs-lookup"><span data-stu-id="49f2a-130">String</span></span>

<span data-ttu-id="49f2a-131">' Table ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="49f2a-131">Parameter 'Table' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="49f2a-132">출력</span><span class="sxs-lookup"><span data-stu-id="49f2a-132">OUTPUTS</span></span>

### <span data-ttu-id="49f2a-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="49f2a-133">System.String</span></span>

## <span data-ttu-id="49f2a-134">상속자</span><span class="sxs-lookup"><span data-stu-id="49f2a-134">NOTES</span></span>

## <span data-ttu-id="49f2a-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="49f2a-135">RELATED LINKS</span></span>

[<span data-ttu-id="49f2a-136">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="49f2a-136">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="49f2a-137">새로운 AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="49f2a-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="49f2a-138">제거-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="49f2a-138">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="49f2a-139">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="49f2a-139">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)


