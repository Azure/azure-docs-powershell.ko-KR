---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BF5526C1-11B9-47A8-A5A6-CB275B470A9E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: b17a294392ca4336d4a96e5d136ad4e321eb45a7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042277"
---
# <span data-ttu-id="b1ec4-101">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b1ec4-101">Get-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="b1ec4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1ec4-102">SYNOPSIS</span></span>
<span data-ttu-id="b1ec4-103">Azure storage 테이블에 대 한 저장 된 액세스 정책 또는 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b1ec4-103">Gets the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="b1ec4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b1ec4-104">SYNTAX</span></span>

```
Get-AzStorageTableStoredAccessPolicy [-Table] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1ec4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b1ec4-105">DESCRIPTION</span></span>
<span data-ttu-id="b1ec4-106">**AzStorageTableStoredAccessPolicy** Cmdlet은 Azure storage 테이블에 대 한 저장 된 액세스 정책 또는 정책을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1ec4-106">The **Get-AzStorageTableStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="b1ec4-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b1ec4-107">EXAMPLES</span></span>

### <span data-ttu-id="b1ec4-108">예제 1: 저장소 테이블에 저장 된 액세스 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="b1ec4-108">Example 1: Get a stored access policy in a storage table</span></span>
```
PS C:\>Get-AzStorageTableStoredAccessPolicy -Table "Table02" -Policy "Policy50"
```

<span data-ttu-id="b1ec4-109">이 명령은 Table02 이라는 저장소 테이블에서 Policy50 라는 액세스 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b1ec4-109">This command gets the access policy named Policy50 in the storage table named Table02.</span></span>

### <span data-ttu-id="b1ec4-110">예제 2: 저장소 테이블에 저장 된 모든 액세스 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="b1ec4-110">Example 2: Get all stored access policies in a storage table</span></span>
```
PS C:\>Get-AzStorageTableStoredAccessPolicy -Table "Table02"
```

<span data-ttu-id="b1ec4-111">이 명령은 Table02 이라는 테이블에 있는 모든 액세스 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b1ec4-111">This command gets all access policies in the table named Table02.</span></span>

## <span data-ttu-id="b1ec4-112">변수</span><span class="sxs-lookup"><span data-stu-id="b1ec4-112">PARAMETERS</span></span>

### <span data-ttu-id="b1ec4-113">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="b1ec4-113">-Context</span></span>
<span data-ttu-id="b1ec4-114">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1ec4-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="b1ec4-115">저장소 컨텍스트를 얻으려면 New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1ec4-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="b1ec4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1ec4-116">-DefaultProfile</span></span>
<span data-ttu-id="b1ec4-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b1ec4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1ec4-118">-정책</span><span class="sxs-lookup"><span data-stu-id="b1ec4-118">-Policy</span></span>
<span data-ttu-id="b1ec4-119">이 SA (공유 액세스 서명) 토큰에 대 한 사용 권한을 포함 하는 저장 된 액세스 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1ec4-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="b1ec4-120">-테이블</span><span class="sxs-lookup"><span data-stu-id="b1ec4-120">-Table</span></span>
<span data-ttu-id="b1ec4-121">Azure 저장소 테이블 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1ec4-121">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="b1ec4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1ec4-122">CommonParameters</span></span>
<span data-ttu-id="b1ec4-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1ec4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1ec4-124">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1ec4-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1ec4-125">입력</span><span class="sxs-lookup"><span data-stu-id="b1ec4-125">INPUTS</span></span>

### <span data-ttu-id="b1ec4-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b1ec4-126">System.String</span></span>

### <span data-ttu-id="b1ec4-127">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b1ec4-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b1ec4-128">출력</span><span class="sxs-lookup"><span data-stu-id="b1ec4-128">OUTPUTS</span></span>

### <span data-ttu-id="b1ec4-129">WindowsAzure. SharedAccessTablePolicy</span><span class="sxs-lookup"><span data-stu-id="b1ec4-129">Microsoft.WindowsAzure.Storage.Table.SharedAccessTablePolicy</span></span>

## <span data-ttu-id="b1ec4-130">상속자</span><span class="sxs-lookup"><span data-stu-id="b1ec4-130">NOTES</span></span>

## <span data-ttu-id="b1ec4-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b1ec4-131">RELATED LINKS</span></span>

[<span data-ttu-id="b1ec4-132">새로운 AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b1ec4-132">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="b1ec4-133">제거-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b1ec4-133">Remove-AzStorageTableStoredAccessPolicy</span></span>](./Remove-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="b1ec4-134">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b1ec4-134">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="b1ec4-135">새로운 AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="b1ec4-135">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


