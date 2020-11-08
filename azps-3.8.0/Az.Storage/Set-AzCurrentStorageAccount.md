---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 15973FE8-16C1-4B71-A3A8-6D6F67A96FDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azcurrentstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzCurrentStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzCurrentStorageAccount.md
ms.openlocfilehash: c57f8a7ce6b4f7275e724c777c2e6dfd54a680ee
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043058"
---
# <span data-ttu-id="4ad0c-101">Set-AzCurrentStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4ad0c-101">Set-AzCurrentStorageAccount</span></span>

## <span data-ttu-id="4ad0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ad0c-102">SYNOPSIS</span></span>
<span data-ttu-id="4ad0c-103">지정 된 구독의 현재 저장소 계정을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad0c-103">Modifies the current Storage account of the specified subscription.</span></span>

## <span data-ttu-id="4ad0c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4ad0c-104">SYNTAX</span></span>

### <span data-ttu-id="4ad0c-105">UsingResourceGroupAndNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="4ad0c-105">UsingResourceGroupAndNameParameterSet (Default)</span></span>
```
Set-AzCurrentStorageAccount -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ad0c-106">UsingStorageContext</span><span class="sxs-lookup"><span data-stu-id="4ad0c-106">UsingStorageContext</span></span>
```
Set-AzCurrentStorageAccount -Context <IStorageContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4ad0c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="4ad0c-107">DESCRIPTION</span></span>
<span data-ttu-id="4ad0c-108">**AzCurrentStorageAccount** Cmdlet은 Azure PowerShell의 지정 된 azure 구독에 대 한 현재 azure 저장소 계정을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad0c-108">The **Set-AzCurrentStorageAccount** cmdlet modifies the current Azure Storage account of the specified Azure subscription in Azure PowerShell.</span></span>
<span data-ttu-id="4ad0c-109">저장소 계정 이름을 지정 하지 않고 저장소에 액세스할 때 현재 저장소 계정이 기본값으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4ad0c-109">The current Storage account is used as the default when you access Storage without specifying a Storage account name.</span></span>

## <span data-ttu-id="4ad0c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="4ad0c-110">EXAMPLES</span></span>

### <span data-ttu-id="4ad0c-111">예제 1: 현재 저장소 계정 설정</span><span class="sxs-lookup"><span data-stu-id="4ad0c-111">Example 1: Set the current Storage account</span></span>
```
PS C:\>Set-AzCurrentStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="4ad0c-112">이 명령은 지정 된 구독에 대 한 기본 저장소 계정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad0c-112">This command sets the default Storage account for the specified subscription.</span></span>

## <span data-ttu-id="4ad0c-113">변수</span><span class="sxs-lookup"><span data-stu-id="4ad0c-113">PARAMETERS</span></span>

### <span data-ttu-id="4ad0c-114">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="4ad0c-114">-Context</span></span>
<span data-ttu-id="4ad0c-115">현재 저장소 계정에 대 한 **Azurestoragecontext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad0c-115">Specifies an **AzureStorageContext** object for the current Storage account.</span></span>
<span data-ttu-id="4ad0c-116">저장소 컨텍스트 개체를 가져오려면 New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad0c-116">To obtain a storage context object, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="4ad0c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ad0c-117">-DefaultProfile</span></span>
<span data-ttu-id="4ad0c-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4ad0c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ad0c-119">-이름</span><span class="sxs-lookup"><span data-stu-id="4ad0c-119">-Name</span></span>
<span data-ttu-id="4ad0c-120">이 cmdlet이 수정 하는 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad0c-120">Specifies the name of the Storage account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="4ad0c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ad0c-121">-ResourceGroupName</span></span>
<span data-ttu-id="4ad0c-122">수정할 저장소 계정이 포함 된 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad0c-122">Specifies the resource group that contains the Storage account to modify.</span></span>

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

### <span data-ttu-id="4ad0c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ad0c-123">CommonParameters</span></span>
<span data-ttu-id="4ad0c-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad0c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ad0c-125">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ad0c-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ad0c-126">입력</span><span class="sxs-lookup"><span data-stu-id="4ad0c-126">INPUTS</span></span>

### <span data-ttu-id="4ad0c-127">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4ad0c-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

### <span data-ttu-id="4ad0c-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4ad0c-128">System.String</span></span>

## <span data-ttu-id="4ad0c-129">출력</span><span class="sxs-lookup"><span data-stu-id="4ad0c-129">OUTPUTS</span></span>

### <span data-ttu-id="4ad0c-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4ad0c-130">System.String</span></span>

## <span data-ttu-id="4ad0c-131">상속자</span><span class="sxs-lookup"><span data-stu-id="4ad0c-131">NOTES</span></span>

## <span data-ttu-id="4ad0c-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4ad0c-132">RELATED LINKS</span></span>

[<span data-ttu-id="4ad0c-133">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4ad0c-133">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)


