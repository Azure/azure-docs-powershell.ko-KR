---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: BF5526C1-11B9-47A8-A5A6-CB275B470A9E
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragetablestoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: a9c141684eb924ed0b969c469214d92b847e13db
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882074"
---
# <span data-ttu-id="cb35f-101">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="cb35f-101">Get-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="cb35f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb35f-102">SYNOPSIS</span></span>
<span data-ttu-id="cb35f-103">Azure storage 테이블에 대 한 저장 된 액세스 정책 또는 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cb35f-103">Gets the stored access policy or policies for an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb35f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cb35f-104">SYNTAX</span></span>

```
Get-AzureStorageTableStoredAccessPolicy [-Table] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb35f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cb35f-105">DESCRIPTION</span></span>
<span data-ttu-id="cb35f-106">**AzureStorageTableStoredAccessPolicy** Cmdlet은 Azure storage 테이블에 대 한 저장 된 액세스 정책 또는 정책을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb35f-106">The **Get-AzureStorageTableStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="cb35f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="cb35f-107">EXAMPLES</span></span>

### <span data-ttu-id="cb35f-108">예제 1: 저장소 테이블에 저장 된 액세스 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="cb35f-108">Example 1: Get a stored access policy in a storage table</span></span>
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02" -Policy "Policy50"
```

<span data-ttu-id="cb35f-109">이 명령은 Table02 이라는 저장소 테이블에서 Policy50 라는 액세스 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cb35f-109">This command gets the access policy named Policy50 in the storage table named Table02.</span></span>

### <span data-ttu-id="cb35f-110">예제 2: 저장소 테이블에 저장 된 모든 액세스 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="cb35f-110">Example 2: Get all stored access policies in a storage table</span></span>
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02"
```

<span data-ttu-id="cb35f-111">이 명령은 Table02 이라는 테이블에 있는 모든 액세스 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cb35f-111">This command gets all access policies in the table named Table02.</span></span>

## <span data-ttu-id="cb35f-112">변수</span><span class="sxs-lookup"><span data-stu-id="cb35f-112">PARAMETERS</span></span>

### <span data-ttu-id="cb35f-113">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="cb35f-113">-Context</span></span>
<span data-ttu-id="cb35f-114">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb35f-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="cb35f-115">저장소 컨텍스트를 얻으려면 New-AzureStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb35f-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb35f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb35f-116">-DefaultProfile</span></span>
<span data-ttu-id="cb35f-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cb35f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb35f-118">-정책</span><span class="sxs-lookup"><span data-stu-id="cb35f-118">-Policy</span></span>
<span data-ttu-id="cb35f-119">이 SA (공유 액세스 서명) 토큰에 대 한 사용 권한을 포함 하는 저장 된 액세스 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb35f-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb35f-120">-테이블</span><span class="sxs-lookup"><span data-stu-id="cb35f-120">-Table</span></span>
<span data-ttu-id="cb35f-121">Azure 저장소 테이블 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb35f-121">Specifies the Azure storage table name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb35f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb35f-122">CommonParameters</span></span>
<span data-ttu-id="cb35f-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb35f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb35f-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb35f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb35f-125">입력</span><span class="sxs-lookup"><span data-stu-id="cb35f-125">INPUTS</span></span>

### <span data-ttu-id="cb35f-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="cb35f-126">System.String</span></span>

### <span data-ttu-id="cb35f-127">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="cb35f-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="cb35f-128">출력</span><span class="sxs-lookup"><span data-stu-id="cb35f-128">OUTPUTS</span></span>

### <span data-ttu-id="cb35f-129">WindowsAzure. SharedAccessTablePolicy</span><span class="sxs-lookup"><span data-stu-id="cb35f-129">Microsoft.WindowsAzure.Storage.Table.SharedAccessTablePolicy</span></span>

## <span data-ttu-id="cb35f-130">상속자</span><span class="sxs-lookup"><span data-stu-id="cb35f-130">NOTES</span></span>

## <span data-ttu-id="cb35f-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cb35f-131">RELATED LINKS</span></span>

[<span data-ttu-id="cb35f-132">새로운 AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="cb35f-132">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="cb35f-133">제거-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="cb35f-133">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="cb35f-134">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="cb35f-134">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="cb35f-135">새로운 AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="cb35f-135">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


