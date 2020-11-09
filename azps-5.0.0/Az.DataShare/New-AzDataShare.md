---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShare.md
ms.openlocfilehash: 265f917068237fee13f77eb8c87e0adf8cd12f08
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305222"
---
# <span data-ttu-id="13472-101">New-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="13472-101">New-AzDataShare</span></span>

## <span data-ttu-id="13472-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13472-102">SYNOPSIS</span></span>
<span data-ttu-id="13472-103">Azure data share를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="13472-103">Creates a azure data share.</span></span>

## <span data-ttu-id="13472-104">구문과</span><span class="sxs-lookup"><span data-stu-id="13472-104">SYNTAX</span></span>

```
New-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-Description <String>]
 [-TermsOfUse <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13472-105">설명은</span><span class="sxs-lookup"><span data-stu-id="13472-105">DESCRIPTION</span></span>
<span data-ttu-id="13472-106">**AzDataShare** cmdlet은 리소스 그룹 이름, 계정 이름, 공유 이름 및 공유 종류를 제공 하 여 지정 된 azure 데이터 공유 계정 내에 데이터 공유를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="13472-106">The **New-AzDataShare** cmdlet creates a data share within a specified azure data share account by providing the resource group name, account name, share name and share kind.</span></span> <span data-ttu-id="13472-107">설명 및 사용 약관은 데이터 공유를 만드는 동안 설정할 수 있는 선택적 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="13472-107">Description and terms of use are optional parameters that can be set while creating the data share.</span></span>

## <span data-ttu-id="13472-108">예제의</span><span class="sxs-lookup"><span data-stu-id="13472-108">EXAMPLES</span></span>

### <span data-ttu-id="13472-109">예제 1: 데이터 공유 만들기</span><span class="sxs-lookup"><span data-stu-id="13472-109">Example 1 : Create a data share</span></span>
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

<span data-ttu-id="13472-110">이 명령은 설명 및 사용 약관을 포함 하 여 리소스 그룹 광고 아래에 있는 데이터 공유 계정 WikiAdsAccount에 기반 하 여 AdsShare 라는 데이터 공유를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="13472-110">This command creates a data share named AdsShare of kind CopyBased in data share account WikiAdsAccount under resource group ADS with description and terms of use.</span></span>

## <span data-ttu-id="13472-111">변수</span><span class="sxs-lookup"><span data-stu-id="13472-111">PARAMETERS</span></span>

### <span data-ttu-id="13472-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="13472-112">-AccountName</span></span>
<span data-ttu-id="13472-113">Azure data share 계정 이름</span><span class="sxs-lookup"><span data-stu-id="13472-113">Azure data share account name</span></span>

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

### <span data-ttu-id="13472-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13472-114">-DefaultProfile</span></span>
<span data-ttu-id="13472-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="13472-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13472-116">-설명</span><span class="sxs-lookup"><span data-stu-id="13472-116">-Description</span></span>
<span data-ttu-id="13472-117">Azure data share에 대 한 설명</span><span class="sxs-lookup"><span data-stu-id="13472-117">Description of azure data share</span></span>

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

### <span data-ttu-id="13472-118">-이름</span><span class="sxs-lookup"><span data-stu-id="13472-118">-Name</span></span>
<span data-ttu-id="13472-119">Azure 데이터 공유 이름</span><span class="sxs-lookup"><span data-stu-id="13472-119">Azure data share name</span></span>

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

### <span data-ttu-id="13472-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13472-120">-ResourceGroupName</span></span>
<span data-ttu-id="13472-121">Azure data share 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="13472-121">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="13472-122">-TermsOfUse</span><span class="sxs-lookup"><span data-stu-id="13472-122">-TermsOfUse</span></span>
<span data-ttu-id="13472-123">Azure data share의 사용 약관</span><span class="sxs-lookup"><span data-stu-id="13472-123">Terms of use for azure data share</span></span>

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

### <span data-ttu-id="13472-124">-확인</span><span class="sxs-lookup"><span data-stu-id="13472-124">-Confirm</span></span>
<span data-ttu-id="13472-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="13472-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13472-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13472-126">-WhatIf</span></span>
<span data-ttu-id="13472-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="13472-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13472-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="13472-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13472-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13472-129">CommonParameters</span></span>
<span data-ttu-id="13472-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="13472-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13472-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="13472-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13472-132">입력</span><span class="sxs-lookup"><span data-stu-id="13472-132">INPUTS</span></span>

### <span data-ttu-id="13472-133">않아야</span><span class="sxs-lookup"><span data-stu-id="13472-133">None</span></span>

## <span data-ttu-id="13472-134">출력</span><span class="sxs-lookup"><span data-stu-id="13472-134">OUTPUTS</span></span>

### <span data-ttu-id="13472-135">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="13472-135">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="13472-136">상속자</span><span class="sxs-lookup"><span data-stu-id="13472-136">NOTES</span></span>

## <span data-ttu-id="13472-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="13472-137">RELATED LINKS</span></span>
