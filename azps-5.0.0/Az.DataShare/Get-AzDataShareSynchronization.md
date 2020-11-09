---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronization.md
ms.openlocfilehash: b60b43b2c0a28be969ad633c80338f42b2c98db6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305240"
---
# <span data-ttu-id="366e0-101">Get-AzDataShareSynchronization</span><span class="sxs-lookup"><span data-stu-id="366e0-101">Get-AzDataShareSynchronization</span></span>

## <span data-ttu-id="366e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="366e0-102">SYNOPSIS</span></span>
<span data-ttu-id="366e0-103">공유에 대 한 동기화 설정에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="366e0-103">Gets information about synchronization setting for a share.</span></span>

## <span data-ttu-id="366e0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="366e0-104">SYNTAX</span></span>

### <span data-ttu-id="366e0-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="366e0-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronization -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="366e0-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="366e0-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronization -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="366e0-107">설명은</span><span class="sxs-lookup"><span data-stu-id="366e0-107">DESCRIPTION</span></span>
<span data-ttu-id="366e0-108">**AzDataShareSynchronization** cmdlet은 데이터 공유 계정으로 공유에 있는 모든 동기화 설정에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="366e0-108">The **Get-AzDataShareSynchronization** cmdlet provides information about all the synchronization setting present in a share under a data share account.</span></span>

## <span data-ttu-id="366e0-109">예제의</span><span class="sxs-lookup"><span data-stu-id="366e0-109">EXAMPLES</span></span>

### <span data-ttu-id="366e0-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="366e0-110">Example 1</span></span>
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

<span data-ttu-id="366e0-111">이 명령은 데이터 공유 계정 WikiAds의 공유 AdsShare에 있는 모든 동기화 설정에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="366e0-111">This commands provides information about all synchronization settings present in share AdsShare in data share account WikiAds.</span></span>

## <span data-ttu-id="366e0-112">변수</span><span class="sxs-lookup"><span data-stu-id="366e0-112">PARAMETERS</span></span>

### <span data-ttu-id="366e0-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="366e0-113">-AccountName</span></span>
<span data-ttu-id="366e0-114">Azure data share 계정 이름</span><span class="sxs-lookup"><span data-stu-id="366e0-114">Azure data share account name</span></span>

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

### <span data-ttu-id="366e0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="366e0-115">-DefaultProfile</span></span>
<span data-ttu-id="366e0-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="366e0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="366e0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="366e0-117">-ResourceGroupName</span></span>
<span data-ttu-id="366e0-118">Azure data share 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="366e0-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="366e0-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="366e0-119">-ResourceId</span></span>
<span data-ttu-id="366e0-120">Azure data share 리소스 id</span><span class="sxs-lookup"><span data-stu-id="366e0-120">Azure data share resource id</span></span>

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

### <span data-ttu-id="366e0-121">-ShareName</span><span class="sxs-lookup"><span data-stu-id="366e0-121">-ShareName</span></span>
<span data-ttu-id="366e0-122">Azure 데이터 공유 이름</span><span class="sxs-lookup"><span data-stu-id="366e0-122">Azure data share name</span></span>

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

### <span data-ttu-id="366e0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="366e0-123">CommonParameters</span></span>
<span data-ttu-id="366e0-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="366e0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="366e0-125">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="366e0-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="366e0-126">입력</span><span class="sxs-lookup"><span data-stu-id="366e0-126">INPUTS</span></span>

### <span data-ttu-id="366e0-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="366e0-127">System.String</span></span>

## <span data-ttu-id="366e0-128">출력</span><span class="sxs-lookup"><span data-stu-id="366e0-128">OUTPUTS</span></span>

### <span data-ttu-id="366e0-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronization 동기화</span><span class="sxs-lookup"><span data-stu-id="366e0-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronization</span></span>

## <span data-ttu-id="366e0-130">상속자</span><span class="sxs-lookup"><span data-stu-id="366e0-130">NOTES</span></span>

## <span data-ttu-id="366e0-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="366e0-131">RELATED LINKS</span></span>
