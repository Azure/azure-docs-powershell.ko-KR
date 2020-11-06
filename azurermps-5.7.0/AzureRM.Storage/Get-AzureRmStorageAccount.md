---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: E53D5040-C1E8-4DC1-8371-F41C00B666E3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccount.md
ms.openlocfilehash: e84bb0dd511f5534b8794327b68f2321efcdc130
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526524"
---
# <span data-ttu-id="b0af9-101">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b0af9-101">Get-AzureRmStorageAccount</span></span>

## <span data-ttu-id="b0af9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0af9-102">SYNOPSIS</span></span>
<span data-ttu-id="b0af9-103">저장소 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b0af9-103">Gets a Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0af9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b0af9-104">SYNTAX</span></span>

### <span data-ttu-id="b0af9-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0af9-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmStorageAccount [[-ResourceGroupName] <String>] [<CommonParameters>]
```

### <span data-ttu-id="b0af9-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0af9-106">AccountNameParameterSet</span></span>
```
Get-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="b0af9-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b0af9-107">DESCRIPTION</span></span>
<span data-ttu-id="b0af9-108">**AzureRmStorageAccount** cmdlet은 지정 된 저장소 계정 또는 리소스 그룹 또는 구독에 있는 모든 저장소 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b0af9-108">The **Get-AzureRmStorageAccount** cmdlet gets a specified Storage account or all of the Storage accounts in a resource group or the subscription.</span></span>

## <span data-ttu-id="b0af9-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b0af9-109">EXAMPLES</span></span>

### <span data-ttu-id="b0af9-110">예제 1: 지정 된 저장소 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="b0af9-110">Example 1: Get a specified storage account</span></span>
```
PS C:\>Get-AzureRmStorageAccount -ResourceGroupName "RG01" -AccountName "MyStorageAccount"
```

<span data-ttu-id="b0af9-111">이 명령은 지정 된 저장소 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b0af9-111">This command gets the specified Storage account.</span></span>

### <span data-ttu-id="b0af9-112">예제 2: 리소스 그룹의 모든 저장소 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="b0af9-112">Example 2: Get all Storage accounts in a resource group</span></span>
```
PS C:\>Get-AzureRmStorageAccount -ResourceGroupName "RG01"
```

<span data-ttu-id="b0af9-113">이 명령은 리소스 그룹의 모든 저장소 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b0af9-113">This command gets all of the Storage accounts in a resource group.</span></span>

### <span data-ttu-id="b0af9-114">예제 3: 구독에서 모든 저장소 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="b0af9-114">Example 3:  Get all Storage accounts in the subscription</span></span>
```
PS C:\>Get-AzureRmStorageAccount
```

<span data-ttu-id="b0af9-115">이 명령은 구독에 있는 모든 저장소 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b0af9-115">This command gets all of the Storage accounts in the subscription.</span></span>

## <span data-ttu-id="b0af9-116">변수</span><span class="sxs-lookup"><span data-stu-id="b0af9-116">PARAMETERS</span></span>

### <span data-ttu-id="b0af9-117">-이름</span><span class="sxs-lookup"><span data-stu-id="b0af9-117">-Name</span></span>
<span data-ttu-id="b0af9-118">가져올 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0af9-118">Specifies the name of the Storage account to get.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0af9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0af9-119">-ResourceGroupName</span></span>
<span data-ttu-id="b0af9-120">가져올 저장소 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0af9-120">Specifies the name of the resource group that contains the Storage account to get.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0af9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0af9-121">CommonParameters</span></span>
<span data-ttu-id="b0af9-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0af9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0af9-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0af9-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0af9-124">입력</span><span class="sxs-lookup"><span data-stu-id="b0af9-124">INPUTS</span></span>

### <span data-ttu-id="b0af9-125">않아야</span><span class="sxs-lookup"><span data-stu-id="b0af9-125">None</span></span>
<span data-ttu-id="b0af9-126">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b0af9-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b0af9-127">출력</span><span class="sxs-lookup"><span data-stu-id="b0af9-127">OUTPUTS</span></span>

## <span data-ttu-id="b0af9-128">상속자</span><span class="sxs-lookup"><span data-stu-id="b0af9-128">NOTES</span></span>

## <span data-ttu-id="b0af9-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b0af9-129">RELATED LINKS</span></span>

[<span data-ttu-id="b0af9-130">새로운 AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b0af9-130">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="b0af9-131">제거-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b0af9-131">Remove-AzureRmStorageAccount</span></span>](./Remove-AzureRmStorageAccount.md)

[<span data-ttu-id="b0af9-132">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b0af9-132">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)
