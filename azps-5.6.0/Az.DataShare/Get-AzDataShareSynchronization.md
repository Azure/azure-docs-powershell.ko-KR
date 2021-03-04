---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/get-azdatasharesynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronization.md
ms.openlocfilehash: a4d3adbcc63eda80bced31523a43cbbad4513205
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990299"
---
# <span data-ttu-id="44fa0-101">Get-AzDataShareSynchronization</span><span class="sxs-lookup"><span data-stu-id="44fa0-101">Get-AzDataShareSynchronization</span></span>

## <span data-ttu-id="44fa0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44fa0-102">SYNOPSIS</span></span>
<span data-ttu-id="44fa0-103">공유에 대한 동기화 설정에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="44fa0-103">Gets information about synchronization setting for a share.</span></span>

## <span data-ttu-id="44fa0-104">구문</span><span class="sxs-lookup"><span data-stu-id="44fa0-104">SYNTAX</span></span>

### <span data-ttu-id="44fa0-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="44fa0-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronization -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44fa0-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="44fa0-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronization -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="44fa0-107">설명</span><span class="sxs-lookup"><span data-stu-id="44fa0-107">DESCRIPTION</span></span>
<span data-ttu-id="44fa0-108">**Get-AzDataShareSynchronization** cmdlet은 데이터 공유 계정 아래 공유에 있는 모든 동기화 설정에 대한 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="44fa0-108">The **Get-AzDataShareSynchronization** cmdlet provides information about all the synchronization setting present in a share under a data share account.</span></span>

## <span data-ttu-id="44fa0-109">예제</span><span class="sxs-lookup"><span data-stu-id="44fa0-109">EXAMPLES</span></span>

### <span data-ttu-id="44fa0-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="44fa0-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare"

Company           : ADS Test
DurationMs        : 107013
EndTime           : 7/8/2019 11:53:18 PM
Message           :
StartTime         : 7/8/2019 11:51:34 PM
Status            : Succeeded
SynchronizationId : e6dc7080-6589-4628-8b50-8fc31b460089
```

<span data-ttu-id="44fa0-111">이 명령은 데이터 공유 계정 WikiAds의 Share AdsShare에 있는 모든 동기화 설정에 대한 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="44fa0-111">This commands provides information about all synchronization settings present in share AdsShare in data share account WikiAds.</span></span>

## <span data-ttu-id="44fa0-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="44fa0-112">PARAMETERS</span></span>

### <span data-ttu-id="44fa0-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="44fa0-113">-AccountName</span></span>
<span data-ttu-id="44fa0-114">Azure 데이터 공유 계정 이름</span><span class="sxs-lookup"><span data-stu-id="44fa0-114">Azure data share account name</span></span>

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

### <span data-ttu-id="44fa0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44fa0-115">-DefaultProfile</span></span>
<span data-ttu-id="44fa0-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="44fa0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44fa0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44fa0-117">-ResourceGroupName</span></span>
<span data-ttu-id="44fa0-118">Azure 데이터 공유 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="44fa0-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="44fa0-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="44fa0-119">-ResourceId</span></span>
<span data-ttu-id="44fa0-120">Azure 데이터 공유 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="44fa0-120">Azure data share resource id</span></span>

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

### <span data-ttu-id="44fa0-121">-ShareName</span><span class="sxs-lookup"><span data-stu-id="44fa0-121">-ShareName</span></span>
<span data-ttu-id="44fa0-122">Azure 데이터 공유 이름</span><span class="sxs-lookup"><span data-stu-id="44fa0-122">Azure data share name</span></span>

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

### <span data-ttu-id="44fa0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44fa0-123">CommonParameters</span></span>
<span data-ttu-id="44fa0-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="44fa0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44fa0-125">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="44fa0-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44fa0-126">입력</span><span class="sxs-lookup"><span data-stu-id="44fa0-126">INPUTS</span></span>

### <span data-ttu-id="44fa0-127">System.String</span><span class="sxs-lookup"><span data-stu-id="44fa0-127">System.String</span></span>

## <span data-ttu-id="44fa0-128">출력</span><span class="sxs-lookup"><span data-stu-id="44fa0-128">OUTPUTS</span></span>

### <span data-ttu-id="44fa0-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronization</span><span class="sxs-lookup"><span data-stu-id="44fa0-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronization</span></span>

## <span data-ttu-id="44fa0-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="44fa0-130">NOTES</span></span>

## <span data-ttu-id="44fa0-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="44fa0-131">RELATED LINKS</span></span>
