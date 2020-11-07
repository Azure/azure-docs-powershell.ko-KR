---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesynchronizationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationDetail.md
ms.openlocfilehash: 8e0f62f4b3d29d0aff9a2bdfcd7916805544af14
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878521"
---
# <span data-ttu-id="bcc77-101">Get-AzDataShareSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="bcc77-101">Get-AzDataShareSynchronizationDetail</span></span>

## <span data-ttu-id="bcc77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bcc77-102">SYNOPSIS</span></span>
<span data-ttu-id="bcc77-103">공유에 대 한 동기화 정보에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bcc77-103">Gets information about synchronization details for a share.</span></span>

## <span data-ttu-id="bcc77-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bcc77-104">SYNTAX</span></span>

### <span data-ttu-id="bcc77-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="bcc77-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronizationDetail -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -SynchronizationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bcc77-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bcc77-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronizationDetail -SynchronizationId <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bcc77-107">설명은</span><span class="sxs-lookup"><span data-stu-id="bcc77-107">DESCRIPTION</span></span>
<span data-ttu-id="bcc77-108">**AzDataShareSynchronizationDetail** cmdlet은 공유에 대해 시작 된 동기화에 대 한 세부 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="bcc77-108">The **Get-AzDataShareSynchronizationDetail** cmdlet provides details of the synchronization initiated for a share.</span></span>

## <span data-ttu-id="bcc77-109">예제의</span><span class="sxs-lookup"><span data-stu-id="bcc77-109">EXAMPLES</span></span>

### <span data-ttu-id="bcc77-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="bcc77-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSynchronizationDetail -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -SynchronizationId "02a17faa-4498-45ee-a884-162180af9251"

DataSetId    : d2411889-5357-4ca8-8d65-9363e46ef2ed
DataSetType  : BlobFolder
EndTime      : 7/8/2019 10:24:27 PM
StartTime    : 7/8/2019 10:23:09 PM
Status       : Succeeded
DurationMs   : 78870
FilesRead    : 1
FilesWritten : 1
SizeRead     : 2779935
SizeWritten  : 2779935
Name         : 16d5161b-2b3f-4d90-b074-13ad7121bcc7
Message      :
```

<span data-ttu-id="bcc77-111">이 명령은 제공 된 동기화 id에 해당 하는 모든 데이터 집합의 동기화 정보에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="bcc77-111">This command provides information about the synchronization details of all the data sets corresponding to the provided synchronization id.</span></span>

## <span data-ttu-id="bcc77-112">변수</span><span class="sxs-lookup"><span data-stu-id="bcc77-112">PARAMETERS</span></span>

### <span data-ttu-id="bcc77-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="bcc77-113">-AccountName</span></span>
<span data-ttu-id="bcc77-114">Azure data share 계정 이름</span><span class="sxs-lookup"><span data-stu-id="bcc77-114">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcc77-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcc77-115">-DefaultProfile</span></span>
<span data-ttu-id="bcc77-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bcc77-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bcc77-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcc77-117">-ResourceGroupName</span></span>
<span data-ttu-id="bcc77-118">Azure data share 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="bcc77-118">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcc77-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bcc77-119">-ResourceId</span></span>
<span data-ttu-id="bcc77-120">Azure data share 리소스 id</span><span class="sxs-lookup"><span data-stu-id="bcc77-120">Azure data share resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcc77-121">-ShareName</span><span class="sxs-lookup"><span data-stu-id="bcc77-121">-ShareName</span></span>
<span data-ttu-id="bcc77-122">Azure 데이터 공유 이름</span><span class="sxs-lookup"><span data-stu-id="bcc77-122">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcc77-123">-SynchronizationId</span><span class="sxs-lookup"><span data-stu-id="bcc77-123">-SynchronizationId</span></span>
<span data-ttu-id="bcc77-124">공유 동기화의 동기화 id</span><span class="sxs-lookup"><span data-stu-id="bcc77-124">Synchronization id of share synchronization</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcc77-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcc77-125">CommonParameters</span></span>
<span data-ttu-id="bcc77-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bcc77-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcc77-127">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcc77-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcc77-128">입력</span><span class="sxs-lookup"><span data-stu-id="bcc77-128">INPUTS</span></span>

### <span data-ttu-id="bcc77-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="bcc77-129">System.String</span></span>

## <span data-ttu-id="bcc77-130">출력</span><span class="sxs-lookup"><span data-stu-id="bcc77-130">OUTPUTS</span></span>

### <span data-ttu-id="bcc77-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="bcc77-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span></span>

## <span data-ttu-id="bcc77-132">상속자</span><span class="sxs-lookup"><span data-stu-id="bcc77-132">NOTES</span></span>

## <span data-ttu-id="bcc77-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bcc77-133">RELATED LINKS</span></span>
