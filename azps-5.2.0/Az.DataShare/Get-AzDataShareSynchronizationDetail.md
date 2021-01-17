---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesynchronizationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationDetail.md
ms.openlocfilehash: 2ee3714895b751223768ac3f98efbd04405ae69f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342045"
---
# <span data-ttu-id="0b275-101">Get-AzDataShareSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="0b275-101">Get-AzDataShareSynchronizationDetail</span></span>

## <span data-ttu-id="0b275-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b275-102">SYNOPSIS</span></span>
<span data-ttu-id="0b275-103">공유에 대한 동기화 세부 정보에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0b275-103">Gets information about synchronization details for a share.</span></span>

## <span data-ttu-id="0b275-104">구문</span><span class="sxs-lookup"><span data-stu-id="0b275-104">SYNTAX</span></span>

### <span data-ttu-id="0b275-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="0b275-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronizationDetail -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -SynchronizationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b275-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b275-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronizationDetail -SynchronizationId <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b275-107">설명</span><span class="sxs-lookup"><span data-stu-id="0b275-107">DESCRIPTION</span></span>
<span data-ttu-id="0b275-108">**Get-AzDataShareSynchronizationDetail** cmdlet은 공유에 대해 시작된 동기화의 세부 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="0b275-108">The **Get-AzDataShareSynchronizationDetail** cmdlet provides details of the synchronization initiated for a share.</span></span>

## <span data-ttu-id="0b275-109">예제</span><span class="sxs-lookup"><span data-stu-id="0b275-109">EXAMPLES</span></span>

### <span data-ttu-id="0b275-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="0b275-110">Example 1</span></span>
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

<span data-ttu-id="0b275-111">이 명령은 제공된 동기화 ID에 해당하는 모든 데이터 집합의 동기화 세부 정보에 대한 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="0b275-111">This command provides information about the synchronization details of all the data sets corresponding to the provided synchronization id.</span></span>

## <span data-ttu-id="0b275-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0b275-112">PARAMETERS</span></span>

### <span data-ttu-id="0b275-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0b275-113">-AccountName</span></span>
<span data-ttu-id="0b275-114">Azure 데이터 공유 계정 이름</span><span class="sxs-lookup"><span data-stu-id="0b275-114">Azure data share account name</span></span>

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

### <span data-ttu-id="0b275-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b275-115">-DefaultProfile</span></span>
<span data-ttu-id="0b275-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0b275-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b275-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b275-117">-ResourceGroupName</span></span>
<span data-ttu-id="0b275-118">Azure 데이터 공유 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="0b275-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="0b275-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0b275-119">-ResourceId</span></span>
<span data-ttu-id="0b275-120">Azure 데이터 공유 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="0b275-120">Azure data share resource id</span></span>

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

### <span data-ttu-id="0b275-121">-ShareName</span><span class="sxs-lookup"><span data-stu-id="0b275-121">-ShareName</span></span>
<span data-ttu-id="0b275-122">Azure 데이터 공유 이름</span><span class="sxs-lookup"><span data-stu-id="0b275-122">Azure data share name</span></span>

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

### <span data-ttu-id="0b275-123">-SynchronizationId</span><span class="sxs-lookup"><span data-stu-id="0b275-123">-SynchronizationId</span></span>
<span data-ttu-id="0b275-124">공유 동기화의 동기화 ID</span><span class="sxs-lookup"><span data-stu-id="0b275-124">Synchronization id of share synchronization</span></span>

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

### <span data-ttu-id="0b275-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b275-125">CommonParameters</span></span>
<span data-ttu-id="0b275-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0b275-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b275-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0b275-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b275-128">입력</span><span class="sxs-lookup"><span data-stu-id="0b275-128">INPUTS</span></span>

### <span data-ttu-id="0b275-129">System.String</span><span class="sxs-lookup"><span data-stu-id="0b275-129">System.String</span></span>

## <span data-ttu-id="0b275-130">출력</span><span class="sxs-lookup"><span data-stu-id="0b275-130">OUTPUTS</span></span>

### <span data-ttu-id="0b275-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="0b275-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span></span>

## <span data-ttu-id="0b275-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0b275-132">NOTES</span></span>

## <span data-ttu-id="0b275-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0b275-133">RELATED LINKS</span></span>
