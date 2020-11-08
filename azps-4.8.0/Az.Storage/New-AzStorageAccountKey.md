---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FDD2CE98-6C7E-4B95-BA5B-B03B6AC6EAEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
ms.openlocfilehash: eebf58120449466ac18231af6daed538ff7da937
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213803"
---
# <span data-ttu-id="be78e-101">New-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="be78e-101">New-AzStorageAccountKey</span></span>

## <span data-ttu-id="be78e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be78e-102">SYNOPSIS</span></span>
<span data-ttu-id="be78e-103">Azure 저장소 계정에 대 한 저장소 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="be78e-103">Regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="be78e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="be78e-104">SYNTAX</span></span>

```
New-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be78e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="be78e-105">DESCRIPTION</span></span>
<span data-ttu-id="be78e-106">**AzStorageAccountKey** Cmdlet은 Azure 저장소 계정에 대 한 저장소 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="be78e-106">The **New-AzStorageAccountKey** cmdlet regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="be78e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="be78e-107">EXAMPLES</span></span>

### <span data-ttu-id="be78e-108">예제 1: 저장소 키 다시 생성</span><span class="sxs-lookup"><span data-stu-id="be78e-108">Example 1: Regenerate a storage key</span></span>
```
PS C:\>New-AzStorageAccountKey -ResourceGroupName "MyResourceGroup" -Name "mystorageaccount" -KeyName "key1"
```

<span data-ttu-id="be78e-109">이 명령은 지정 된 저장소 계정에 대 한 저장소 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="be78e-109">This command regenerates a storage key for the specified Storage account.</span></span>

## <span data-ttu-id="be78e-110">변수</span><span class="sxs-lookup"><span data-stu-id="be78e-110">PARAMETERS</span></span>

### <span data-ttu-id="be78e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be78e-111">-DefaultProfile</span></span>
<span data-ttu-id="be78e-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="be78e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be78e-113">-KeyName</span><span class="sxs-lookup"><span data-stu-id="be78e-113">-KeyName</span></span>
<span data-ttu-id="be78e-114">재생성할 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be78e-114">Specifies which key to regenerate.</span></span>
<span data-ttu-id="be78e-115">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="be78e-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="be78e-116">key1</span><span class="sxs-lookup"><span data-stu-id="be78e-116">key1</span></span>
- <span data-ttu-id="be78e-117">key2</span><span class="sxs-lookup"><span data-stu-id="be78e-117">key2</span></span>
- <span data-ttu-id="be78e-118">kerb1</span><span class="sxs-lookup"><span data-stu-id="be78e-118">kerb1</span></span>
- <span data-ttu-id="be78e-119">kerb2</span><span class="sxs-lookup"><span data-stu-id="be78e-119">kerb2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: key1, key2, kerb1, kerb2

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be78e-120">-이름</span><span class="sxs-lookup"><span data-stu-id="be78e-120">-Name</span></span>
<span data-ttu-id="be78e-121">저장소 키를 다시 생성할 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be78e-121">Specifies the name of the Storage account for which to regenerate a storage key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be78e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be78e-122">-ResourceGroupName</span></span>
<span data-ttu-id="be78e-123">저장소 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be78e-123">Specifies the name of the resource group that contains the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be78e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be78e-124">CommonParameters</span></span>
<span data-ttu-id="be78e-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="be78e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be78e-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be78e-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be78e-127">입력</span><span class="sxs-lookup"><span data-stu-id="be78e-127">INPUTS</span></span>

### <span data-ttu-id="be78e-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="be78e-128">System.String</span></span>

## <span data-ttu-id="be78e-129">출력</span><span class="sxs-lookup"><span data-stu-id="be78e-129">OUTPUTS</span></span>

### <span data-ttu-id="be78e-130">StorageAccountListKeysResult를 통해 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="be78e-130">Microsoft.Azure.Management.Storage.Models.StorageAccountListKeysResult</span></span>

## <span data-ttu-id="be78e-131">상속자</span><span class="sxs-lookup"><span data-stu-id="be78e-131">NOTES</span></span>

## <span data-ttu-id="be78e-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="be78e-132">RELATED LINKS</span></span>

[<span data-ttu-id="be78e-133">Get-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="be78e-133">Get-AzStorageAccountKey</span></span>](./Get-AzStorageAccountKey.md)
