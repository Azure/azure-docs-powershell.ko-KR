---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageUsage.md
ms.openlocfilehash: c63573da3c12eb54329d05f49615057d0595b77c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531321"
---
# <span data-ttu-id="be2a2-101">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="be2a2-101">Get-AzureRmStorageUsage</span></span>

## <span data-ttu-id="be2a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be2a2-102">SYNOPSIS</span></span>
<span data-ttu-id="be2a2-103">현재 구독의 저장소 리소스 사용량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="be2a2-103">Gets the Storage resource usage of the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be2a2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="be2a2-104">SYNTAX</span></span>

```
Get-AzureRmStorageUsage [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be2a2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="be2a2-105">DESCRIPTION</span></span>
<span data-ttu-id="be2a2-106">**AzureRmStorageUsage** cmdlet은 현재 구독에 대 한 Azure 저장소의 리소스 사용량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="be2a2-106">The **Get-AzureRmStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="be2a2-107">예제의</span><span class="sxs-lookup"><span data-stu-id="be2a2-107">EXAMPLES</span></span>

### <span data-ttu-id="be2a2-108">예제 1: 저장소 리소스 사용 현황 가져오기</span><span class="sxs-lookup"><span data-stu-id="be2a2-108">Example 1: Get the storage resources usage</span></span>
```
PS C:\>Get-AzureRmStorageUsage
```

<span data-ttu-id="be2a2-109">이 명령은 현재 구독의 저장소 리소스 사용 현황을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="be2a2-109">This command gets the Storage resources usage of the current subscription.</span></span>
 

### <span data-ttu-id="be2a2-110">예제 2: 지정 된 위치의 저장소 리소스 사용 현황 가져오기</span><span class="sxs-lookup"><span data-stu-id="be2a2-110">Example 2: Get the storage resources usage of specified location</span></span>
```
PS C:\>Get-AzureRmStorageUsage -Location 'West US'

LocalizedName : Storage Accounts
Name          : StorageAccounts
Unit          : Count
CurrentValue  : 18
Limit         : 250
```

<span data-ttu-id="be2a2-111">이 명령은 현재 구독에서 지정 된 위치의 저장소 리소스 사용량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="be2a2-111">This command gets the Storage resources usage of the specified location under the current subscription.</span></span>

## <span data-ttu-id="be2a2-112">변수</span><span class="sxs-lookup"><span data-stu-id="be2a2-112">PARAMETERS</span></span>

### <span data-ttu-id="be2a2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be2a2-113">-DefaultProfile</span></span>
<span data-ttu-id="be2a2-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="be2a2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be2a2-115">-위치</span><span class="sxs-lookup"><span data-stu-id="be2a2-115">-Location</span></span>
<span data-ttu-id="be2a2-116">지정 된 위치에서 저장소 리소스 사용량을 가져오는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="be2a2-116">Indicate to get Storage resources usage on the specified location.</span></span>
<span data-ttu-id="be2a2-117">지정 하지 않으면 구독 아래의 모든 위치에서 저장소 리소스 사용량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="be2a2-117">If not specified, will get Storage resources usage on all locations under the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be2a2-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be2a2-118">CommonParameters</span></span>
<span data-ttu-id="be2a2-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="be2a2-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be2a2-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be2a2-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be2a2-121">입력</span><span class="sxs-lookup"><span data-stu-id="be2a2-121">INPUTS</span></span>

### <span data-ttu-id="be2a2-122">않아야</span><span class="sxs-lookup"><span data-stu-id="be2a2-122">None</span></span>

## <span data-ttu-id="be2a2-123">출력</span><span class="sxs-lookup"><span data-stu-id="be2a2-123">OUTPUTS</span></span>

### <span data-ttu-id="be2a2-124">Microsoft. Azure. i m//. m a i 사용</span><span class="sxs-lookup"><span data-stu-id="be2a2-124">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span></span>

## <span data-ttu-id="be2a2-125">상속자</span><span class="sxs-lookup"><span data-stu-id="be2a2-125">NOTES</span></span>

## <span data-ttu-id="be2a2-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="be2a2-126">RELATED LINKS</span></span>

[<span data-ttu-id="be2a2-127">Azure 저장소 관리자 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="be2a2-127">Azure Storage Manager Cmdlets</span></span>](./AzureRM.Storage.md)


