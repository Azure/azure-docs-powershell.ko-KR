---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
ms.openlocfilehash: 31729843425f2360f1716e2b0faffc72715b9a81
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698639"
---
# <span data-ttu-id="16d41-101">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="16d41-101">Get-AzStorageUsage</span></span>

## <span data-ttu-id="16d41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16d41-102">SYNOPSIS</span></span>
<span data-ttu-id="16d41-103">현재 구독의 저장소 리소스 사용량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="16d41-103">Gets the Storage resource usage of the current subscription.</span></span>

## <span data-ttu-id="16d41-104">구문과</span><span class="sxs-lookup"><span data-stu-id="16d41-104">SYNTAX</span></span>

```
Get-AzStorageUsage -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16d41-105">설명은</span><span class="sxs-lookup"><span data-stu-id="16d41-105">DESCRIPTION</span></span>
<span data-ttu-id="16d41-106">**AzStorageUsage** cmdlet은 현재 구독에 대 한 Azure 저장소의 리소스 사용량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="16d41-106">The **Get-AzStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="16d41-107">예제의</span><span class="sxs-lookup"><span data-stu-id="16d41-107">EXAMPLES</span></span>

### <span data-ttu-id="16d41-108">예제 1: 지정 된 위치의 저장소 리소스 사용 가져오기</span><span class="sxs-lookup"><span data-stu-id="16d41-108">Example 1: Get the storage resources usage of specified location</span></span>
```
PS C:\>Get-AzStorageUsage -Location 'West US'

LocalizedName : Storage Accounts
Name          : StorageAccounts
Unit          : Count
CurrentValue  : 18
Limit         : 250
```

<span data-ttu-id="16d41-109">이 명령은 현재 구독에서 지정 된 위치의 저장소 리소스 사용량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="16d41-109">This command gets the Storage resources usage of the specified location under the current subscription.</span></span>

## <span data-ttu-id="16d41-110">변수</span><span class="sxs-lookup"><span data-stu-id="16d41-110">PARAMETERS</span></span>

### <span data-ttu-id="16d41-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16d41-111">-DefaultProfile</span></span>
<span data-ttu-id="16d41-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="16d41-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16d41-113">-위치</span><span class="sxs-lookup"><span data-stu-id="16d41-113">-Location</span></span>
<span data-ttu-id="16d41-114">지정 된 위치에서 저장소 리소스 사용량을 가져오는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="16d41-114">Indicate to get Storage resources usage on the specified location.</span></span>
<span data-ttu-id="16d41-115">지정 하지 않으면 구독 아래의 모든 위치에서 저장소 리소스 사용량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="16d41-115">If not specified, will get Storage resources usage on all locations under the subscription.</span></span>

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

### <span data-ttu-id="16d41-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16d41-116">CommonParameters</span></span>
<span data-ttu-id="16d41-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="16d41-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16d41-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16d41-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16d41-119">입력</span><span class="sxs-lookup"><span data-stu-id="16d41-119">INPUTS</span></span>

### <span data-ttu-id="16d41-120">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="16d41-120">System.String</span></span>

## <span data-ttu-id="16d41-121">출력</span><span class="sxs-lookup"><span data-stu-id="16d41-121">OUTPUTS</span></span>

### <span data-ttu-id="16d41-122">Microsoft. Azure. i m//. m a i 사용</span><span class="sxs-lookup"><span data-stu-id="16d41-122">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span></span>

## <span data-ttu-id="16d41-123">상속자</span><span class="sxs-lookup"><span data-stu-id="16d41-123">NOTES</span></span>

## <span data-ttu-id="16d41-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="16d41-124">RELATED LINKS</span></span>

[<span data-ttu-id="16d41-125">Azure 저장소 관리자 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="16d41-125">Azure Storage Manager Cmdlets</span></span>](./Az.Storage.md)


