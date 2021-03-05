---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
ms.openlocfilehash: 9e12aa08bd37a5dfa467b2df03df42f5c58e4186
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994779"
---
# <span data-ttu-id="b4590-101">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="b4590-101">Get-AzStorageUsage</span></span>

## <span data-ttu-id="b4590-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4590-102">SYNOPSIS</span></span>
<span data-ttu-id="b4590-103">현재 구독의 Storage 리소스 사용량을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b4590-103">Gets the Storage resource usage of the current subscription.</span></span>

## <span data-ttu-id="b4590-104">구문</span><span class="sxs-lookup"><span data-stu-id="b4590-104">SYNTAX</span></span>

```
Get-AzStorageUsage -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4590-105">설명</span><span class="sxs-lookup"><span data-stu-id="b4590-105">DESCRIPTION</span></span>
<span data-ttu-id="b4590-106">**Get-AzStorageUsage** cmdlet은 현재 구독에 대한 Azure Storage에 대한 리소스 사용량을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b4590-106">The **Get-AzStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="b4590-107">예제</span><span class="sxs-lookup"><span data-stu-id="b4590-107">EXAMPLES</span></span>

### <span data-ttu-id="b4590-108">예제 1: 지정된 위치의 저장소 리소스 사용량을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b4590-108">Example 1: Get the storage resources usage of specified location</span></span>
```
PS C:\>Get-AzStorageUsage -Location 'West US'

LocalizedName : Storage Accounts
Name          : StorageAccounts
Unit          : Count
CurrentValue  : 18
Limit         : 250
```

<span data-ttu-id="b4590-109">이 명령은 현재 구독에서 지정된 위치의 Storage 리소스 사용량을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b4590-109">This command gets the Storage resources usage of specified location under the current subscription.</span></span>

## <span data-ttu-id="b4590-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b4590-110">PARAMETERS</span></span>

### <span data-ttu-id="b4590-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4590-111">-DefaultProfile</span></span>
<span data-ttu-id="b4590-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b4590-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4590-113">-Location</span><span class="sxs-lookup"><span data-stu-id="b4590-113">-Location</span></span>
<span data-ttu-id="b4590-114">지정된 위치에서 Storage 리소스 사용량을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b4590-114">Indicate to get Storage resources usage on the specified location.</span></span>
<span data-ttu-id="b4590-115">지정하지 않으면 구독의 모든 위치에 Storage 리소스 사용량이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b4590-115">If not specified, will get Storage resources usage on all locations under the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4590-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4590-116">CommonParameters</span></span>
<span data-ttu-id="b4590-117">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b4590-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4590-118">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b4590-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4590-119">입력</span><span class="sxs-lookup"><span data-stu-id="b4590-119">INPUTS</span></span>

### <span data-ttu-id="b4590-120">System.String</span><span class="sxs-lookup"><span data-stu-id="b4590-120">System.String</span></span>

## <span data-ttu-id="b4590-121">출력</span><span class="sxs-lookup"><span data-stu-id="b4590-121">OUTPUTS</span></span>

### <span data-ttu-id="b4590-122">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span><span class="sxs-lookup"><span data-stu-id="b4590-122">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span></span>

## <span data-ttu-id="b4590-123">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b4590-123">NOTES</span></span>

## <span data-ttu-id="b4590-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b4590-124">RELATED LINKS</span></span>

[<span data-ttu-id="b4590-125">Azure Storage Manager Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b4590-125">Azure Storage Manager Cmdlets</span></span>](./Az.Storage.md)


