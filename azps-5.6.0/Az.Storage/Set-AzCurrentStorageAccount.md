---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 15973FE8-16C1-4B71-A3A8-6D6F67A96FDF
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azcurrentstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzCurrentStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzCurrentStorageAccount.md
ms.openlocfilehash: aeda6548526c4ad12746ce90f1a030f85a0a8d2d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950784"
---
# <span data-ttu-id="b5d6c-101">Set-AzCurrentStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b5d6c-101">Set-AzCurrentStorageAccount</span></span>

## <span data-ttu-id="b5d6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5d6c-102">SYNOPSIS</span></span>
<span data-ttu-id="b5d6c-103">지정된 구독의 현재 Storage 계정을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="b5d6c-103">Modifies the current Storage account of the specified subscription.</span></span>

## <span data-ttu-id="b5d6c-104">구문</span><span class="sxs-lookup"><span data-stu-id="b5d6c-104">SYNTAX</span></span>

### <span data-ttu-id="b5d6c-105">UsingResourceGroupAndNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="b5d6c-105">UsingResourceGroupAndNameParameterSet (Default)</span></span>
```
Set-AzCurrentStorageAccount -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5d6c-106">UsingStorageContext</span><span class="sxs-lookup"><span data-stu-id="b5d6c-106">UsingStorageContext</span></span>
```
Set-AzCurrentStorageAccount -Context <IStorageContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b5d6c-107">설명</span><span class="sxs-lookup"><span data-stu-id="b5d6c-107">DESCRIPTION</span></span>
<span data-ttu-id="b5d6c-108">**Set-AzCurrentStorageAccount** cmdlet은 Azure PowerShell에서 지정된 Azure 구독의 현재 Azure Storage 계정을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="b5d6c-108">The **Set-AzCurrentStorageAccount** cmdlet modifies the current Azure Storage account of the specified Azure subscription in Azure PowerShell.</span></span>
<span data-ttu-id="b5d6c-109">현재 Storage 계정은 Storage 계정 이름을 지정하지 않고 Storage에 액세스할 때 기본값으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="b5d6c-109">The current Storage account is used as the default when you access Storage without specifying a Storage account name.</span></span>

## <span data-ttu-id="b5d6c-110">예제</span><span class="sxs-lookup"><span data-stu-id="b5d6c-110">EXAMPLES</span></span>

### <span data-ttu-id="b5d6c-111">예제 1: 현재 Storage 계정 설정</span><span class="sxs-lookup"><span data-stu-id="b5d6c-111">Example 1: Set the current Storage account</span></span>
```
PS C:\>Set-AzCurrentStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="b5d6c-112">이 명령은 지정된 구독에 대한 기본 Storage 계정을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="b5d6c-112">This command sets the default Storage account for the specified subscription.</span></span>

## <span data-ttu-id="b5d6c-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b5d6c-113">PARAMETERS</span></span>

### <span data-ttu-id="b5d6c-114">-Context</span><span class="sxs-lookup"><span data-stu-id="b5d6c-114">-Context</span></span>
<span data-ttu-id="b5d6c-115">현재 Storage 계정에 **대한 AzureStorageContext** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b5d6c-115">Specifies an **AzureStorageContext** object for the current Storage account.</span></span>
<span data-ttu-id="b5d6c-116">저장소 컨텍스트 개체를 얻은 경우 New-AzStorageContext cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="b5d6c-116">To obtain a storage context object, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: UsingStorageContext
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5d6c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5d6c-117">-DefaultProfile</span></span>
<span data-ttu-id="b5d6c-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b5d6c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5d6c-119">-Name</span><span class="sxs-lookup"><span data-stu-id="b5d6c-119">-Name</span></span>
<span data-ttu-id="b5d6c-120">이 cmdlet이 수정하는 Storage 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b5d6c-120">Specifies the name of the Storage account that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: UsingResourceGroupAndNameParameterSet
Aliases: StorageAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5d6c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5d6c-121">-ResourceGroupName</span></span>
<span data-ttu-id="b5d6c-122">수정할 Storage 계정이 포함된 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b5d6c-122">Specifies the resource group that contains the Storage account to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: UsingResourceGroupAndNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5d6c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5d6c-123">CommonParameters</span></span>
<span data-ttu-id="b5d6c-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b5d6c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5d6c-125">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b5d6c-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5d6c-126">입력</span><span class="sxs-lookup"><span data-stu-id="b5d6c-126">INPUTS</span></span>

### <span data-ttu-id="b5d6c-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b5d6c-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

### <span data-ttu-id="b5d6c-128">System.String</span><span class="sxs-lookup"><span data-stu-id="b5d6c-128">System.String</span></span>

## <span data-ttu-id="b5d6c-129">출력</span><span class="sxs-lookup"><span data-stu-id="b5d6c-129">OUTPUTS</span></span>

### <span data-ttu-id="b5d6c-130">System.String</span><span class="sxs-lookup"><span data-stu-id="b5d6c-130">System.String</span></span>

## <span data-ttu-id="b5d6c-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b5d6c-131">NOTES</span></span>

## <span data-ttu-id="b5d6c-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b5d6c-132">RELATED LINKS</span></span>

[<span data-ttu-id="b5d6c-133">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b5d6c-133">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)


