---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: CF3B6E3B-3FC1-4871-AFE0-366B17A9E4F8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 54b28caaf39bd3d4750e341da4f4564d60b59138
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523023"
---
# <span data-ttu-id="88e0c-101">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="88e0c-101">New-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="88e0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88e0c-102">SYNOPSIS</span></span>
<span data-ttu-id="88e0c-103">Azure storage 테이블에 대 한 저장 된 액세스 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="88e0c-103">Creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="88e0c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="88e0c-104">SYNTAX</span></span>

```
New-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="88e0c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="88e0c-105">DESCRIPTION</span></span>
<span data-ttu-id="88e0c-106">**AzureStorageTableStoredAccessPolicy** Cmdlet은 Azure storage 테이블에 대해 저장 된 액세스 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="88e0c-106">The **New-AzureStorageTableStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="88e0c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="88e0c-107">EXAMPLES</span></span>

### <span data-ttu-id="88e0c-108">예제 1: 테이블에 저장 된 액세스 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="88e0c-108">Example 1: Create a stored access policy in a table</span></span>
```
PS C:\>New-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy02"
```

<span data-ttu-id="88e0c-109">이 명령은 MyTable 이라는 저장소 테이블에 Policy02 라는 액세스 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="88e0c-109">This command creates an access policy named Policy02 in the storage table named MyTable.</span></span>

## <span data-ttu-id="88e0c-110">변수</span><span class="sxs-lookup"><span data-stu-id="88e0c-110">PARAMETERS</span></span>

### <span data-ttu-id="88e0c-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="88e0c-111">-Context</span></span>
<span data-ttu-id="88e0c-112">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88e0c-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="88e0c-113">저장소 컨텍스트를 얻으려면 New-AzureStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="88e0c-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="88e0c-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="88e0c-114">-ExpiryTime</span></span>
<span data-ttu-id="88e0c-115">저장 된 액세스 정책이 무효화 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88e0c-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="88e0c-116">-사용 권한</span><span class="sxs-lookup"><span data-stu-id="88e0c-116">-Permission</span></span>
<span data-ttu-id="88e0c-117">이 저장소 테이블에 대 한 공용 액세스 수준을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88e0c-117">Specifies the level of public access to this storage table.</span></span>

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

### <span data-ttu-id="88e0c-118">-정책</span><span class="sxs-lookup"><span data-stu-id="88e0c-118">-Policy</span></span>
<span data-ttu-id="88e0c-119">이 SA (공유 액세스 서명) 토큰에 대 한 사용 권한을 포함 하는 저장 된 액세스 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88e0c-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="88e0c-120">-StartTime</span><span class="sxs-lookup"><span data-stu-id="88e0c-120">-StartTime</span></span>
<span data-ttu-id="88e0c-121">저장 된 액세스 정책이 유효 하 게 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88e0c-121">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="88e0c-122">-테이블</span><span class="sxs-lookup"><span data-stu-id="88e0c-122">-Table</span></span>
<span data-ttu-id="88e0c-123">Azure 저장소 테이블 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88e0c-123">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="88e0c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88e0c-124">CommonParameters</span></span>
<span data-ttu-id="88e0c-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="88e0c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88e0c-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88e0c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88e0c-127">입력</span><span class="sxs-lookup"><span data-stu-id="88e0c-127">INPUTS</span></span>

## <span data-ttu-id="88e0c-128">출력</span><span class="sxs-lookup"><span data-stu-id="88e0c-128">OUTPUTS</span></span>

## <span data-ttu-id="88e0c-129">상속자</span><span class="sxs-lookup"><span data-stu-id="88e0c-129">NOTES</span></span>

## <span data-ttu-id="88e0c-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="88e0c-130">RELATED LINKS</span></span>

[<span data-ttu-id="88e0c-131">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="88e0c-131">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="88e0c-132">새로운 AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="88e0c-132">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="88e0c-133">제거-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="88e0c-133">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="88e0c-134">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="88e0c-134">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)


