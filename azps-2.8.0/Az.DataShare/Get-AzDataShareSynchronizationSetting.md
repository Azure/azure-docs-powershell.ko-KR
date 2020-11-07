---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: 9dca6272991c67375f2764725901018c331e0ca9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696721"
---
# <span data-ttu-id="39faa-101">Get-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="39faa-101">Get-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="39faa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39faa-102">SYNOPSIS</span></span>
<span data-ttu-id="39faa-103">공유의 동기화 설정에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="39faa-103">Gets information about synchronization setting on a share.</span></span>

## <span data-ttu-id="39faa-104">구문과</span><span class="sxs-lookup"><span data-stu-id="39faa-104">SYNTAX</span></span>

### <span data-ttu-id="39faa-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="39faa-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39faa-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="39faa-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronizationSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="39faa-107">설명은</span><span class="sxs-lookup"><span data-stu-id="39faa-107">DESCRIPTION</span></span>
<span data-ttu-id="39faa-108">**AzDataShareSynchronizationSetting** cmdlet은 공유에서 사용 하도록 설정 된 동기화에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="39faa-108">The **Get-AzDataShareSynchronizationSetting** cmdlet provides information about synchronization enabled on a share.</span></span> 

## <span data-ttu-id="39faa-109">예제의</span><span class="sxs-lookup"><span data-stu-id="39faa-109">EXAMPLES</span></span>

### <span data-ttu-id="39faa-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="39faa-110">Example 1</span></span>
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

<span data-ttu-id="39faa-111">이 명령은 data 공유 계정 WikiAds에서 ShareSynchronization 공유에서 사용 하도록 설정 된 동기화에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="39faa-111">This command provides information about synchronization ShareSynchronization enabled on share AdsShare under data share account WikiAds.</span></span>

## <span data-ttu-id="39faa-112">변수</span><span class="sxs-lookup"><span data-stu-id="39faa-112">PARAMETERS</span></span>

### <span data-ttu-id="39faa-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="39faa-113">-AccountName</span></span>
<span data-ttu-id="39faa-114">Azure data share 계정 이름</span><span class="sxs-lookup"><span data-stu-id="39faa-114">Azure data share account name</span></span>

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

### <span data-ttu-id="39faa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39faa-115">-DefaultProfile</span></span>
<span data-ttu-id="39faa-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="39faa-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39faa-117">-이름</span><span class="sxs-lookup"><span data-stu-id="39faa-117">-Name</span></span>
<span data-ttu-id="39faa-118">동기화 설정의 이름</span><span class="sxs-lookup"><span data-stu-id="39faa-118">Name for Synchronization Setting</span></span>

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

### <span data-ttu-id="39faa-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39faa-119">-ResourceGroupName</span></span>
<span data-ttu-id="39faa-120">Azure data share 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="39faa-120">Resource group name of azure data share account</span></span>

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

### <span data-ttu-id="39faa-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="39faa-121">-ResourceId</span></span>
<span data-ttu-id="39faa-122">Azure 데이터 공유 동기화 설정의 리소스 id</span><span class="sxs-lookup"><span data-stu-id="39faa-122">The resource id of the azure data share synchronization setting</span></span>

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

### <span data-ttu-id="39faa-123">-ShareName</span><span class="sxs-lookup"><span data-stu-id="39faa-123">-ShareName</span></span>
<span data-ttu-id="39faa-124">Azure 데이터 공유 이름</span><span class="sxs-lookup"><span data-stu-id="39faa-124">Azure data share name</span></span>

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

### <span data-ttu-id="39faa-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39faa-125">CommonParameters</span></span>
<span data-ttu-id="39faa-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="39faa-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39faa-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39faa-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39faa-128">입력</span><span class="sxs-lookup"><span data-stu-id="39faa-128">INPUTS</span></span>

### <span data-ttu-id="39faa-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="39faa-129">System.String</span></span>

## <span data-ttu-id="39faa-130">출력</span><span class="sxs-lookup"><span data-stu-id="39faa-130">OUTPUTS</span></span>

### <span data-ttu-id="39faa-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="39faa-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="39faa-132">상속자</span><span class="sxs-lookup"><span data-stu-id="39faa-132">NOTES</span></span>

## <span data-ttu-id="39faa-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="39faa-133">RELATED LINKS</span></span>
