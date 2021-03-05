---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FDD2CE98-6C7E-4B95-BA5B-B03B6AC6EAEF
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
ms.openlocfilehash: 254d9a012bd3539242e560511e23975acb68b4bf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002656"
---
# <span data-ttu-id="e655b-101">New-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="e655b-101">New-AzStorageAccountKey</span></span>

## <span data-ttu-id="e655b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e655b-102">SYNOPSIS</span></span>
<span data-ttu-id="e655b-103">Azure Storage 계정에 대한 저장소 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="e655b-103">Regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="e655b-104">구문</span><span class="sxs-lookup"><span data-stu-id="e655b-104">SYNTAX</span></span>

```
New-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e655b-105">설명</span><span class="sxs-lookup"><span data-stu-id="e655b-105">DESCRIPTION</span></span>
<span data-ttu-id="e655b-106">**New-AzStorageAccountKey** cmdlet은 Azure Storage 계정에 대한 저장소 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="e655b-106">The **New-AzStorageAccountKey** cmdlet regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="e655b-107">예제</span><span class="sxs-lookup"><span data-stu-id="e655b-107">EXAMPLES</span></span>

### <span data-ttu-id="e655b-108">예제 1: 저장소 키 다시 생성</span><span class="sxs-lookup"><span data-stu-id="e655b-108">Example 1: Regenerate a storage key</span></span>
```
PS C:\>New-AzStorageAccountKey -ResourceGroupName "MyResourceGroup" -Name "mystorageaccount" -KeyName "key1"
```

<span data-ttu-id="e655b-109">이 명령은 지정된 Storage 계정에 대한 저장소 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="e655b-109">This command regenerates a storage key for the specified Storage account.</span></span>

## <span data-ttu-id="e655b-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e655b-110">PARAMETERS</span></span>

### <span data-ttu-id="e655b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e655b-111">-DefaultProfile</span></span>
<span data-ttu-id="e655b-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e655b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e655b-113">-KeyName</span><span class="sxs-lookup"><span data-stu-id="e655b-113">-KeyName</span></span>
<span data-ttu-id="e655b-114">다시 생성할 키를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e655b-114">Specifies which key to regenerate.</span></span>
<span data-ttu-id="e655b-115">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="e655b-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e655b-116">key1</span><span class="sxs-lookup"><span data-stu-id="e655b-116">key1</span></span>
- <span data-ttu-id="e655b-117">key2</span><span class="sxs-lookup"><span data-stu-id="e655b-117">key2</span></span>
- <span data-ttu-id="e655b-118">kerb1</span><span class="sxs-lookup"><span data-stu-id="e655b-118">kerb1</span></span>
- <span data-ttu-id="e655b-119">kerb2</span><span class="sxs-lookup"><span data-stu-id="e655b-119">kerb2</span></span>

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

### <span data-ttu-id="e655b-120">-Name</span><span class="sxs-lookup"><span data-stu-id="e655b-120">-Name</span></span>
<span data-ttu-id="e655b-121">저장소 키를 다시 생성하는 Storage 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e655b-121">Specifies the name of the Storage account for which to regenerate a storage key.</span></span>

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

### <span data-ttu-id="e655b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e655b-122">-ResourceGroupName</span></span>
<span data-ttu-id="e655b-123">Storage 계정을 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e655b-123">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="e655b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e655b-124">CommonParameters</span></span>
<span data-ttu-id="e655b-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e655b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e655b-126">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e655b-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e655b-127">입력</span><span class="sxs-lookup"><span data-stu-id="e655b-127">INPUTS</span></span>

### <span data-ttu-id="e655b-128">System.String</span><span class="sxs-lookup"><span data-stu-id="e655b-128">System.String</span></span>

## <span data-ttu-id="e655b-129">출력</span><span class="sxs-lookup"><span data-stu-id="e655b-129">OUTPUTS</span></span>

### <span data-ttu-id="e655b-130">Microsoft.Azure.Management.Storage.Models.StorageAccountListKeysResult</span><span class="sxs-lookup"><span data-stu-id="e655b-130">Microsoft.Azure.Management.Storage.Models.StorageAccountListKeysResult</span></span>

## <span data-ttu-id="e655b-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e655b-131">NOTES</span></span>

## <span data-ttu-id="e655b-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e655b-132">RELATED LINKS</span></span>

[<span data-ttu-id="e655b-133">Get-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="e655b-133">Get-AzStorageAccountKey</span></span>](./Get-AzStorageAccountKey.md)
