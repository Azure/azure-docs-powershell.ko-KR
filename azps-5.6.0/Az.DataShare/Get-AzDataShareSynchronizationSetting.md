---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/get-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: 55e887ed60eaf4dd4fc6c26423686b99572702ea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006784"
---
# <span data-ttu-id="6cf8b-101">Get-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="6cf8b-101">Get-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="6cf8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6cf8b-102">SYNOPSIS</span></span>
<span data-ttu-id="6cf8b-103">공유의 동기화 설정에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6cf8b-103">Gets information about synchronization setting on a share.</span></span>

## <span data-ttu-id="6cf8b-104">구문</span><span class="sxs-lookup"><span data-stu-id="6cf8b-104">SYNTAX</span></span>

### <span data-ttu-id="6cf8b-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="6cf8b-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6cf8b-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cf8b-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronizationSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6cf8b-107">설명</span><span class="sxs-lookup"><span data-stu-id="6cf8b-107">DESCRIPTION</span></span>
<span data-ttu-id="6cf8b-108">**Get-AzDataShareSynchronizationSetting** cmdlet은 공유에서 사용하도록 설정된 동기화에 대한 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="6cf8b-108">The **Get-AzDataShareSynchronizationSetting** cmdlet provides information about synchronization enabled on a share.</span></span> 

## <span data-ttu-id="6cf8b-109">예제</span><span class="sxs-lookup"><span data-stu-id="6cf8b-109">EXAMPLES</span></span>

### <span data-ttu-id="6cf8b-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="6cf8b-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSynchronizationSetting -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "ShareSynchronization"

RecurrenceInterval  : Day
SynchronizationTime : 7/9/2019 9:00:00 AM
ProvisioningState   : Succeeded
CreatedAt           : 7/10/2019 12:01:08 AM
CreatedBy           : ADS Test
Id                  : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.
                      DataShare/accounts/WikiAds/shares/AdShare/synchronizationSettings/ShareSynchronization
Name                : ShareSynchronization
Type                : Microsoft.DataShare/SynchronizationSettings
```

<span data-ttu-id="6cf8b-111">이 명령은 데이터 공유 계정 WikiAds에서 Share AdsShare에서 사용하도록 설정된 동기화 ShareSynchronization에 대한 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="6cf8b-111">This command provides information about synchronization ShareSynchronization enabled on share AdsShare under data share account WikiAds.</span></span>

## <span data-ttu-id="6cf8b-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6cf8b-112">PARAMETERS</span></span>

### <span data-ttu-id="6cf8b-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6cf8b-113">-AccountName</span></span>
<span data-ttu-id="6cf8b-114">Azure 데이터 공유 계정 이름</span><span class="sxs-lookup"><span data-stu-id="6cf8b-114">Azure data share account name</span></span>

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

### <span data-ttu-id="6cf8b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cf8b-115">-DefaultProfile</span></span>
<span data-ttu-id="6cf8b-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6cf8b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6cf8b-117">-Name</span><span class="sxs-lookup"><span data-stu-id="6cf8b-117">-Name</span></span>
<span data-ttu-id="6cf8b-118">동기화 설정의 이름</span><span class="sxs-lookup"><span data-stu-id="6cf8b-118">Name for Synchronization Setting</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cf8b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cf8b-119">-ResourceGroupName</span></span>
<span data-ttu-id="6cf8b-120">Azure 데이터 공유 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="6cf8b-120">Resource group name of azure data share account</span></span>

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

### <span data-ttu-id="6cf8b-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6cf8b-121">-ResourceId</span></span>
<span data-ttu-id="6cf8b-122">Azure 데이터 공유 동기화 설정의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="6cf8b-122">The resource id of the azure data share synchronization setting</span></span>

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

### <span data-ttu-id="6cf8b-123">-ShareName</span><span class="sxs-lookup"><span data-stu-id="6cf8b-123">-ShareName</span></span>
<span data-ttu-id="6cf8b-124">Azure 데이터 공유 이름</span><span class="sxs-lookup"><span data-stu-id="6cf8b-124">Azure data share name</span></span>

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

### <span data-ttu-id="6cf8b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cf8b-125">CommonParameters</span></span>
<span data-ttu-id="6cf8b-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6cf8b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cf8b-127">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6cf8b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cf8b-128">입력</span><span class="sxs-lookup"><span data-stu-id="6cf8b-128">INPUTS</span></span>

### <span data-ttu-id="6cf8b-129">System.String</span><span class="sxs-lookup"><span data-stu-id="6cf8b-129">System.String</span></span>

## <span data-ttu-id="6cf8b-130">출력</span><span class="sxs-lookup"><span data-stu-id="6cf8b-130">OUTPUTS</span></span>

### <span data-ttu-id="6cf8b-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="6cf8b-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="6cf8b-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6cf8b-132">NOTES</span></span>

## <span data-ttu-id="6cf8b-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6cf8b-133">RELATED LINKS</span></span>
