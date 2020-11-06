---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 15973FE8-16C1-4B71-A3A8-6D6F67A96FDF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/set-azurermcurrentstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Set-AzureRmCurrentStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Set-AzureRmCurrentStorageAccount.md
ms.openlocfilehash: 5915ce06b6d97dd13f7299f243c2d3df38930f50
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531316"
---
# <span data-ttu-id="9ac7b-101">Set-AzureRmCurrentStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9ac7b-101">Set-AzureRmCurrentStorageAccount</span></span>

## <span data-ttu-id="9ac7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ac7b-102">SYNOPSIS</span></span>
<span data-ttu-id="9ac7b-103">지정 된 구독의 현재 저장소 계정을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac7b-103">Modifies the current Storage account of the specified subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ac7b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9ac7b-104">SYNTAX</span></span>

### <span data-ttu-id="9ac7b-105">UsingResourceGroupAndNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="9ac7b-105">UsingResourceGroupAndNameParameterSet (Default)</span></span>
```
Set-AzureRmCurrentStorageAccount -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ac7b-106">UsingStorageContext</span><span class="sxs-lookup"><span data-stu-id="9ac7b-106">UsingStorageContext</span></span>
```
Set-AzureRmCurrentStorageAccount -Context <IStorageContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9ac7b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="9ac7b-107">DESCRIPTION</span></span>
<span data-ttu-id="9ac7b-108">**AzureRmCurrentStorageAccount** Cmdlet은 Azure PowerShell의 지정 된 azure 구독에 대 한 현재 azure 저장소 계정을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac7b-108">The **Set-AzureRmCurrentStorageAccount** cmdlet modifies the current Azure Storage account of the specified Azure subscription in Azure PowerShell.</span></span>
<span data-ttu-id="9ac7b-109">저장소 계정 이름을 지정 하지 않고 저장소에 액세스할 때 현재 저장소 계정이 기본값으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9ac7b-109">The current Storage account is used as the default when you access Storage without specifying a Storage account name.</span></span>

## <span data-ttu-id="9ac7b-110">예제의</span><span class="sxs-lookup"><span data-stu-id="9ac7b-110">EXAMPLES</span></span>

### <span data-ttu-id="9ac7b-111">예제 1: 현재 저장소 계정 설정</span><span class="sxs-lookup"><span data-stu-id="9ac7b-111">Example 1: Set the current Storage account</span></span>
```
PS C:\>Set-AzureRmCurrentStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="9ac7b-112">이 명령은 지정 된 구독에 대 한 기본 저장소 계정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac7b-112">This command sets the default Storage account for the specified subscription.</span></span>

## <span data-ttu-id="9ac7b-113">변수</span><span class="sxs-lookup"><span data-stu-id="9ac7b-113">PARAMETERS</span></span>

### <span data-ttu-id="9ac7b-114">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="9ac7b-114">-Context</span></span>
<span data-ttu-id="9ac7b-115">현재 저장소 계정에 대 한 **Azurestoragecontext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac7b-115">Specifies an **AzureStorageContext** object for the current Storage account.</span></span>
<span data-ttu-id="9ac7b-116">저장소 컨텍스트 개체를 가져오려면 New-AzureStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac7b-116">To obtain a storage context object, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="9ac7b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ac7b-117">-DefaultProfile</span></span>
<span data-ttu-id="9ac7b-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9ac7b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ac7b-119">-이름</span><span class="sxs-lookup"><span data-stu-id="9ac7b-119">-Name</span></span>
<span data-ttu-id="9ac7b-120">이 cmdlet이 수정 하는 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac7b-120">Specifies the name of the Storage account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="9ac7b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ac7b-121">-ResourceGroupName</span></span>
<span data-ttu-id="9ac7b-122">수정할 저장소 계정이 포함 된 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac7b-122">Specifies the resource group that contains the Storage account to modify.</span></span>

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

### <span data-ttu-id="9ac7b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ac7b-123">CommonParameters</span></span>
<span data-ttu-id="9ac7b-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac7b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ac7b-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ac7b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ac7b-126">입력</span><span class="sxs-lookup"><span data-stu-id="9ac7b-126">INPUTS</span></span>

### <span data-ttu-id="9ac7b-127">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="9ac7b-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

### <span data-ttu-id="9ac7b-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9ac7b-128">System.String</span></span>

## <span data-ttu-id="9ac7b-129">출력</span><span class="sxs-lookup"><span data-stu-id="9ac7b-129">OUTPUTS</span></span>

### <span data-ttu-id="9ac7b-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9ac7b-130">System.String</span></span>

## <span data-ttu-id="9ac7b-131">상속자</span><span class="sxs-lookup"><span data-stu-id="9ac7b-131">NOTES</span></span>

## <span data-ttu-id="9ac7b-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9ac7b-132">RELATED LINKS</span></span>

[<span data-ttu-id="9ac7b-133">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9ac7b-133">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)


