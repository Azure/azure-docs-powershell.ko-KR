---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: FDD2CE98-6C7E-4B95-BA5B-B03B6AC6EAEF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/New-AzureRmStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/New-AzureRmStorageAccountKey.md
ms.openlocfilehash: 76b7ea9eb4a248071025ef359d6bf0877b35fe89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537796"
---
# <span data-ttu-id="d8788-101">New-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="d8788-101">New-AzureRmStorageAccountKey</span></span>

## <span data-ttu-id="d8788-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8788-102">SYNOPSIS</span></span>
<span data-ttu-id="d8788-103">Azure 저장소 계정에 대 한 저장소 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8788-103">Regenerates a storage key for an Azure Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8788-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d8788-104">SYNTAX</span></span>

```
New-AzureRmStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8788-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d8788-105">DESCRIPTION</span></span>
<span data-ttu-id="d8788-106">**AzureRmStorageAccountKey** Cmdlet은 Azure 저장소 계정에 대 한 저장소 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8788-106">The **New-AzureRmStorageAccountKey** cmdlet regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="d8788-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d8788-107">EXAMPLES</span></span>

### <span data-ttu-id="d8788-108">예제 1: 저장소 키 다시 생성</span><span class="sxs-lookup"><span data-stu-id="d8788-108">Example 1: Regenerate a storage key</span></span>
```
PS C:\>New-AzureRmStorageAccountKey -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -KeyName "key1"
```

<span data-ttu-id="d8788-109">이 명령은 지정 된 저장소 계정에 대 한 저장소 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8788-109">This command regenerates a storage key for the specified Storage account.</span></span>

## <span data-ttu-id="d8788-110">변수</span><span class="sxs-lookup"><span data-stu-id="d8788-110">PARAMETERS</span></span>

### <span data-ttu-id="d8788-111">-KeyName</span><span class="sxs-lookup"><span data-stu-id="d8788-111">-KeyName</span></span>
<span data-ttu-id="d8788-112">재생성할 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8788-112">Specifies which key to regenerate.</span></span>
<span data-ttu-id="d8788-113">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d8788-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d8788-114">key1</span><span class="sxs-lookup"><span data-stu-id="d8788-114">key1</span></span> 
- <span data-ttu-id="d8788-115">key2</span><span class="sxs-lookup"><span data-stu-id="d8788-115">key2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: key1, key2

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8788-116">-이름</span><span class="sxs-lookup"><span data-stu-id="d8788-116">-Name</span></span>
<span data-ttu-id="d8788-117">저장소 키를 다시 생성할 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8788-117">Specifies the name of the Storage account for which to regenerate a storage key.</span></span>

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

### <span data-ttu-id="d8788-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8788-118">-ResourceGroupName</span></span>
<span data-ttu-id="d8788-119">저장소 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8788-119">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="d8788-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8788-120">-DefaultProfile</span></span>
<span data-ttu-id="d8788-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d8788-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8788-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8788-122">CommonParameters</span></span>
<span data-ttu-id="d8788-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8788-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8788-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8788-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8788-125">입력</span><span class="sxs-lookup"><span data-stu-id="d8788-125">INPUTS</span></span>

## <span data-ttu-id="d8788-126">출력</span><span class="sxs-lookup"><span data-stu-id="d8788-126">OUTPUTS</span></span>

## <span data-ttu-id="d8788-127">상속자</span><span class="sxs-lookup"><span data-stu-id="d8788-127">NOTES</span></span>

## <span data-ttu-id="d8788-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d8788-128">RELATED LINKS</span></span>

[<span data-ttu-id="d8788-129">Get-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="d8788-129">Get-AzureRmStorageAccountKey</span></span>](./Get-AzureRmStorageAccountKey.md)


