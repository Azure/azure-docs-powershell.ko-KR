---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: FDD2CE98-6C7E-4B95-BA5B-B03B6AC6EAEF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccountKey.md
ms.openlocfilehash: 651fdef0599a9a62de5d4bdfac8fc5e9105bb4dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532592"
---
# <span data-ttu-id="fa478-101">New-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="fa478-101">New-AzureRmStorageAccountKey</span></span>

## <span data-ttu-id="fa478-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa478-102">SYNOPSIS</span></span>
<span data-ttu-id="fa478-103">Azure 저장소 계정에 대 한 저장소 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa478-103">Regenerates a storage key for an Azure Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa478-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fa478-104">SYNTAX</span></span>

```
New-AzureRmStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="fa478-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fa478-105">DESCRIPTION</span></span>
<span data-ttu-id="fa478-106">**AzureRmStorageAccountKey** Cmdlet은 Azure 저장소 계정에 대 한 저장소 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa478-106">The **New-AzureRmStorageAccountKey** cmdlet regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="fa478-107">예제의</span><span class="sxs-lookup"><span data-stu-id="fa478-107">EXAMPLES</span></span>

### <span data-ttu-id="fa478-108">예제 1: 저장소 키 다시 생성</span><span class="sxs-lookup"><span data-stu-id="fa478-108">Example 1: Regenerate a storage key</span></span>
```
PS C:\>New-AzureRmStorageAccountKey -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -KeyName "key1"
```

<span data-ttu-id="fa478-109">이 명령은 지정 된 저장소 계정에 대 한 저장소 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa478-109">This command regenerates a storage key for the specified Storage account.</span></span>

## <span data-ttu-id="fa478-110">변수</span><span class="sxs-lookup"><span data-stu-id="fa478-110">PARAMETERS</span></span>

### <span data-ttu-id="fa478-111">-KeyName</span><span class="sxs-lookup"><span data-stu-id="fa478-111">-KeyName</span></span>
<span data-ttu-id="fa478-112">재생성할 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa478-112">Specifies which key to regenerate.</span></span>
<span data-ttu-id="fa478-113">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="fa478-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fa478-114">key1</span><span class="sxs-lookup"><span data-stu-id="fa478-114">key1</span></span>
- <span data-ttu-id="fa478-115">key2</span><span class="sxs-lookup"><span data-stu-id="fa478-115">key2</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: key1, key2

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa478-116">-이름</span><span class="sxs-lookup"><span data-stu-id="fa478-116">-Name</span></span>
<span data-ttu-id="fa478-117">저장소 키를 다시 생성할 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa478-117">Specifies the name of the Storage account for which to regenerate a storage key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa478-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa478-118">-ResourceGroupName</span></span>
<span data-ttu-id="fa478-119">저장소 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa478-119">Specifies the name of the resource group that contains the Storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa478-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa478-120">CommonParameters</span></span>
<span data-ttu-id="fa478-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa478-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa478-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa478-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa478-123">입력</span><span class="sxs-lookup"><span data-stu-id="fa478-123">INPUTS</span></span>

### <span data-ttu-id="fa478-124">않아야</span><span class="sxs-lookup"><span data-stu-id="fa478-124">None</span></span>
<span data-ttu-id="fa478-125">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fa478-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fa478-126">출력</span><span class="sxs-lookup"><span data-stu-id="fa478-126">OUTPUTS</span></span>

## <span data-ttu-id="fa478-127">상속자</span><span class="sxs-lookup"><span data-stu-id="fa478-127">NOTES</span></span>

## <span data-ttu-id="fa478-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fa478-128">RELATED LINKS</span></span>

[<span data-ttu-id="fa478-129">Get-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="fa478-129">Get-AzureRmStorageAccountKey</span></span>](./Get-AzureRmStorageAccountKey.md)
