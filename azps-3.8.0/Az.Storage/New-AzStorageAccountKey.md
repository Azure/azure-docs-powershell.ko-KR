---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FDD2CE98-6C7E-4B95-BA5B-B03B6AC6EAEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
ms.openlocfilehash: d63c948e59dbc05122c63b6688277a7015a42163
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043145"
---
# <span data-ttu-id="a3b26-101">New-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="a3b26-101">New-AzStorageAccountKey</span></span>

## <span data-ttu-id="a3b26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3b26-102">SYNOPSIS</span></span>
<span data-ttu-id="a3b26-103">Azure 저장소 계정에 대 한 저장소 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3b26-103">Regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="a3b26-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a3b26-104">SYNTAX</span></span>

```
New-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3b26-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a3b26-105">DESCRIPTION</span></span>
<span data-ttu-id="a3b26-106">**AzStorageAccountKey** Cmdlet은 Azure 저장소 계정에 대 한 저장소 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3b26-106">The **New-AzStorageAccountKey** cmdlet regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="a3b26-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a3b26-107">EXAMPLES</span></span>

### <span data-ttu-id="a3b26-108">예제 1: 저장소 키 다시 생성</span><span class="sxs-lookup"><span data-stu-id="a3b26-108">Example 1: Regenerate a storage key</span></span>
```
PS C:\>New-AzStorageAccountKey -ResourceGroupName "MyResourceGroup" -Name "mystorageaccount" -KeyName "key1"
```

<span data-ttu-id="a3b26-109">이 명령은 지정 된 저장소 계정에 대 한 저장소 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3b26-109">This command regenerates a storage key for the specified Storage account.</span></span>

## <span data-ttu-id="a3b26-110">변수</span><span class="sxs-lookup"><span data-stu-id="a3b26-110">PARAMETERS</span></span>

### <span data-ttu-id="a3b26-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3b26-111">-DefaultProfile</span></span>
<span data-ttu-id="a3b26-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a3b26-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3b26-113">-KeyName</span><span class="sxs-lookup"><span data-stu-id="a3b26-113">-KeyName</span></span>
<span data-ttu-id="a3b26-114">재생성할 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3b26-114">Specifies which key to regenerate.</span></span>
<span data-ttu-id="a3b26-115">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a3b26-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a3b26-116">key1</span><span class="sxs-lookup"><span data-stu-id="a3b26-116">key1</span></span>
- <span data-ttu-id="a3b26-117">key2</span><span class="sxs-lookup"><span data-stu-id="a3b26-117">key2</span></span>

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

### <span data-ttu-id="a3b26-118">-이름</span><span class="sxs-lookup"><span data-stu-id="a3b26-118">-Name</span></span>
<span data-ttu-id="a3b26-119">저장소 키를 다시 생성할 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3b26-119">Specifies the name of the Storage account for which to regenerate a storage key.</span></span>

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

### <span data-ttu-id="a3b26-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3b26-120">-ResourceGroupName</span></span>
<span data-ttu-id="a3b26-121">저장소 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3b26-121">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="a3b26-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3b26-122">CommonParameters</span></span>
<span data-ttu-id="a3b26-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3b26-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3b26-124">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3b26-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3b26-125">입력</span><span class="sxs-lookup"><span data-stu-id="a3b26-125">INPUTS</span></span>

### <span data-ttu-id="a3b26-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a3b26-126">System.String</span></span>

## <span data-ttu-id="a3b26-127">출력</span><span class="sxs-lookup"><span data-stu-id="a3b26-127">OUTPUTS</span></span>

### <span data-ttu-id="a3b26-128">StorageAccountListKeysResult를 통해 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3b26-128">Microsoft.Azure.Management.Storage.Models.StorageAccountListKeysResult</span></span>

## <span data-ttu-id="a3b26-129">상속자</span><span class="sxs-lookup"><span data-stu-id="a3b26-129">NOTES</span></span>

## <span data-ttu-id="a3b26-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a3b26-130">RELATED LINKS</span></span>

[<span data-ttu-id="a3b26-131">Get-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="a3b26-131">Get-AzStorageAccountKey</span></span>](./Get-AzStorageAccountKey.md)
