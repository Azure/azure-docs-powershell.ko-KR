---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/new-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShare.md
ms.openlocfilehash: cda809b8c6c4425a3df7bd4ba5ae40a9292e358f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998349"
---
# <span data-ttu-id="70313-101">New-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="70313-101">New-AzDataShare</span></span>

## <span data-ttu-id="70313-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70313-102">SYNOPSIS</span></span>
<span data-ttu-id="70313-103">Azure 데이터 공유를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="70313-103">Creates a azure data share.</span></span>

## <span data-ttu-id="70313-104">구문</span><span class="sxs-lookup"><span data-stu-id="70313-104">SYNTAX</span></span>

```
New-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-Description <String>]
 [-TermsOfUse <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70313-105">설명</span><span class="sxs-lookup"><span data-stu-id="70313-105">DESCRIPTION</span></span>
<span data-ttu-id="70313-106">**New-AzDataShare** cmdlet은 리소스 그룹 이름, 계정 이름, 공유 이름 및 공유 종류를 제공하여 지정된 Azure 데이터 공유 계정 내에서 데이터 공유를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="70313-106">The **New-AzDataShare** cmdlet creates a data share within a specified azure data share account by providing the resource group name, account name, share name and share kind.</span></span> <span data-ttu-id="70313-107">설명 및 사용 약관은 데이터 공유를 만드는 동안 설정할 수 있는 선택적 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="70313-107">Description and terms of use are optional parameters that can be set while creating the data share.</span></span>

## <span data-ttu-id="70313-108">예제</span><span class="sxs-lookup"><span data-stu-id="70313-108">EXAMPLES</span></span>

### <span data-ttu-id="70313-109">예제 1 : 데이터 공유 만들기</span><span class="sxs-lookup"><span data-stu-id="70313-109">Example 1 : Create a data share</span></span>
```
PS C:\>New-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -Name "AdsShare" -ShareKind "CopyBased" -Description "Example of description" -TermsOfUse "This should not be shared"
Name                : AdsShare
Id                  : /subscriptions/f3ead1ff-d0ab-4cf4-9a5a-86f1661d4685/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shares/AdsShare
Type                : Microsoft.DataShare/shares
CreatedAt           : 6/11/2019 12:00:00 AM
CreatedBy           : Contoso ADS
ShareKind           : CopyBased
Description         : Example of description  
ProvisioningState   : Succeeded
Terms               : This should not be shared
```

<span data-ttu-id="70313-110">이 명령은 설명 및 사용 약관이 있는 리소스 그룹 ADS 아래에서 데이터 공유 계정 WikiAdsAccount에서 AdsShare라는 종류의 CopyBased라는 데이터 공유를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="70313-110">This command creates a data share named AdsShare of kind CopyBased in data share account WikiAdsAccount under resource group ADS with description and terms of use.</span></span>

## <span data-ttu-id="70313-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="70313-111">PARAMETERS</span></span>

### <span data-ttu-id="70313-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="70313-112">-AccountName</span></span>
<span data-ttu-id="70313-113">Azure 데이터 공유 계정 이름</span><span class="sxs-lookup"><span data-stu-id="70313-113">Azure data share account name</span></span>

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

### <span data-ttu-id="70313-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70313-114">-DefaultProfile</span></span>
<span data-ttu-id="70313-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="70313-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70313-116">-Description</span><span class="sxs-lookup"><span data-stu-id="70313-116">-Description</span></span>
<span data-ttu-id="70313-117">Azure 데이터 공유에 대한 설명</span><span class="sxs-lookup"><span data-stu-id="70313-117">Description of azure data share</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70313-118">-Name</span><span class="sxs-lookup"><span data-stu-id="70313-118">-Name</span></span>
<span data-ttu-id="70313-119">Azure 데이터 공유 이름</span><span class="sxs-lookup"><span data-stu-id="70313-119">Azure data share name</span></span>

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

### <span data-ttu-id="70313-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70313-120">-ResourceGroupName</span></span>
<span data-ttu-id="70313-121">Azure 데이터 공유 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="70313-121">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="70313-122">-TermsOfUse</span><span class="sxs-lookup"><span data-stu-id="70313-122">-TermsOfUse</span></span>
<span data-ttu-id="70313-123">Azure 데이터 공유에 대한 사용 약관</span><span class="sxs-lookup"><span data-stu-id="70313-123">Terms of use for azure data share</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70313-124">-확인</span><span class="sxs-lookup"><span data-stu-id="70313-124">-Confirm</span></span>
<span data-ttu-id="70313-125">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="70313-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70313-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70313-126">-WhatIf</span></span>
<span data-ttu-id="70313-127">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="70313-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70313-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="70313-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70313-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70313-129">CommonParameters</span></span>
<span data-ttu-id="70313-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="70313-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70313-131">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="70313-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70313-132">입력</span><span class="sxs-lookup"><span data-stu-id="70313-132">INPUTS</span></span>

### <span data-ttu-id="70313-133">없음</span><span class="sxs-lookup"><span data-stu-id="70313-133">None</span></span>

## <span data-ttu-id="70313-134">출력</span><span class="sxs-lookup"><span data-stu-id="70313-134">OUTPUTS</span></span>

### <span data-ttu-id="70313-135">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="70313-135">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="70313-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="70313-136">NOTES</span></span>

## <span data-ttu-id="70313-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="70313-137">RELATED LINKS</span></span>
