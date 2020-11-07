---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BF5526C1-11B9-47A8-A5A6-CB275B470A9E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: c079b65dc0a37ea07815e2e3b47799b9a194f4e2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876285"
---
# <span data-ttu-id="14b37-101">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="14b37-101">Get-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="14b37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14b37-102">SYNOPSIS</span></span>
<span data-ttu-id="14b37-103">Azure storage 테이블에 대 한 저장 된 액세스 정책 또는 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="14b37-103">Gets the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="14b37-104">구문과</span><span class="sxs-lookup"><span data-stu-id="14b37-104">SYNTAX</span></span>

```
Get-AzStorageTableStoredAccessPolicy [-Table] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14b37-105">설명은</span><span class="sxs-lookup"><span data-stu-id="14b37-105">DESCRIPTION</span></span>
<span data-ttu-id="14b37-106">**AzStorageTableStoredAccessPolicy** Cmdlet은 Azure storage 테이블에 대 한 저장 된 액세스 정책 또는 정책을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="14b37-106">The **Get-AzStorageTableStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="14b37-107">예제의</span><span class="sxs-lookup"><span data-stu-id="14b37-107">EXAMPLES</span></span>

### <span data-ttu-id="14b37-108">예제 1: 저장소 테이블에 저장 된 액세스 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="14b37-108">Example 1: Get a stored access policy in a storage table</span></span>
```
PS C:\>Get-AzStorageTableStoredAccessPolicy -Table "Table02" -Policy "Policy50"
```

<span data-ttu-id="14b37-109">이 명령은 Table02 이라는 저장소 테이블에서 Policy50 라는 액세스 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="14b37-109">This command gets the access policy named Policy50 in the storage table named Table02.</span></span>

### <span data-ttu-id="14b37-110">예제 2: 저장소 테이블에 저장 된 모든 액세스 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="14b37-110">Example 2: Get all stored access policies in a storage table</span></span>
```
PS C:\>Get-AzStorageTableStoredAccessPolicy -Table "Table02"
```

<span data-ttu-id="14b37-111">이 명령은 Table02 이라는 테이블에 있는 모든 액세스 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="14b37-111">This command gets all access policies in the table named Table02.</span></span>

## <span data-ttu-id="14b37-112">변수</span><span class="sxs-lookup"><span data-stu-id="14b37-112">PARAMETERS</span></span>

### <span data-ttu-id="14b37-113">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="14b37-113">-Context</span></span>
<span data-ttu-id="14b37-114">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14b37-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="14b37-115">저장소 컨텍스트를 얻으려면 New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="14b37-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="14b37-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14b37-116">-DefaultProfile</span></span>
<span data-ttu-id="14b37-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="14b37-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14b37-118">-정책</span><span class="sxs-lookup"><span data-stu-id="14b37-118">-Policy</span></span>
<span data-ttu-id="14b37-119">이 SA (공유 액세스 서명) 토큰에 대 한 사용 권한을 포함 하는 저장 된 액세스 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14b37-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="14b37-120">-테이블</span><span class="sxs-lookup"><span data-stu-id="14b37-120">-Table</span></span>
<span data-ttu-id="14b37-121">Azure 저장소 테이블 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14b37-121">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="14b37-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14b37-122">CommonParameters</span></span>
<span data-ttu-id="14b37-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="14b37-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14b37-124">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14b37-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14b37-125">입력</span><span class="sxs-lookup"><span data-stu-id="14b37-125">INPUTS</span></span>

### <span data-ttu-id="14b37-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="14b37-126">System.String</span></span>

### <span data-ttu-id="14b37-127">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="14b37-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="14b37-128">출력</span><span class="sxs-lookup"><span data-stu-id="14b37-128">OUTPUTS</span></span>

### <span data-ttu-id="14b37-129">SharedAccessTablePolicy (Microsoft. 테이블.</span><span class="sxs-lookup"><span data-stu-id="14b37-129">Microsoft.WindowsAz.Storage.Table.SharedAccessTablePolicy</span></span>

## <span data-ttu-id="14b37-130">상속자</span><span class="sxs-lookup"><span data-stu-id="14b37-130">NOTES</span></span>

## <span data-ttu-id="14b37-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="14b37-131">RELATED LINKS</span></span>

[<span data-ttu-id="14b37-132">새로운 AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="14b37-132">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="14b37-133">제거-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="14b37-133">Remove-AzStorageTableStoredAccessPolicy</span></span>](./Remove-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="14b37-134">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="14b37-134">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="14b37-135">새로운 AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="14b37-135">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


