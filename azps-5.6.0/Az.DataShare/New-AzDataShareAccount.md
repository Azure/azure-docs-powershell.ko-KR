---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/new-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareAccount.md
ms.openlocfilehash: 91f6c56849d5b8ca96af2a28191cefde803f63c6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986099"
---
# <span data-ttu-id="63e92-101">New-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="63e92-101">New-AzDataShareAccount</span></span>

## <span data-ttu-id="63e92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63e92-102">SYNOPSIS</span></span>
<span data-ttu-id="63e92-103">새 데이터 공유 계정 생성</span><span class="sxs-lookup"><span data-stu-id="63e92-103">Creates new data share account</span></span>

## <span data-ttu-id="63e92-104">구문</span><span class="sxs-lookup"><span data-stu-id="63e92-104">SYNTAX</span></span>

```
New-AzDataShareAccount -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63e92-105">설명</span><span class="sxs-lookup"><span data-stu-id="63e92-105">DESCRIPTION</span></span>
<span data-ttu-id="63e92-106">**New-AzDataShareAccount** cmdlet은 지정된 Azure 리소스 그룹에 데이터 공유 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="63e92-106">**New-AzDataShareAccount** cmdlet creates a datashare account in the specified Azure resource group.</span></span>

## <span data-ttu-id="63e92-107">예제</span><span class="sxs-lookup"><span data-stu-id="63e92-107">EXAMPLES</span></span>

### <span data-ttu-id="63e92-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="63e92-108">Example 1</span></span>
```
PS C:\> New-AzDataShareAccount -ResourceGroupName "ADS" -Name "WikiADS" -Location "WestUS"
DataShareAccountName   : WikiADS
ResourceGroupName : ADS
Location          : WestUS
ProvisioningState : Succeeded
Tags              : {}
Identity          : Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSIdentity
Type              : Microsoft.DataShare/accounts
Id                : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiADS
```

<span data-ttu-id="63e92-109">리소스 그룹 "ADS"에서 "WikiADS"라는 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="63e92-109">Creates an account named "WikiADS" in resource group "ADS"</span></span>

## <span data-ttu-id="63e92-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="63e92-110">PARAMETERS</span></span>

### <span data-ttu-id="63e92-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="63e92-111">-AsJob</span></span>
<span data-ttu-id="63e92-112">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="63e92-112">{{Fill AsJob Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63e92-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63e92-113">-DefaultProfile</span></span>
<span data-ttu-id="63e92-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="63e92-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63e92-115">-Location</span><span class="sxs-lookup"><span data-stu-id="63e92-115">-Location</span></span>
<span data-ttu-id="63e92-116">데이터 공유 계정을 만들 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="63e92-116">The location in which to create the data share account.</span></span>

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

### <span data-ttu-id="63e92-117">-Name</span><span class="sxs-lookup"><span data-stu-id="63e92-117">-Name</span></span>
<span data-ttu-id="63e92-118">Azure 데이터 공유 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="63e92-118">Azure data share account name.</span></span>

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

### <span data-ttu-id="63e92-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63e92-119">-ResourceGroupName</span></span>
<span data-ttu-id="63e92-120">Azure 데이터 공유 계정의 리소스 그룹 이름이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="63e92-120">The resource group name of the azure data share account will be created in.</span></span>

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

### <span data-ttu-id="63e92-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="63e92-121">-Tag</span></span>
<span data-ttu-id="63e92-122">Azure 데이터 공유 계정과 연결되는 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="63e92-122">The tags to associate with the azure data share account.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63e92-123">-확인</span><span class="sxs-lookup"><span data-stu-id="63e92-123">-Confirm</span></span>
<span data-ttu-id="63e92-124">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="63e92-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63e92-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63e92-125">-WhatIf</span></span>
<span data-ttu-id="63e92-126">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="63e92-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63e92-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="63e92-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63e92-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63e92-128">CommonParameters</span></span>
<span data-ttu-id="63e92-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="63e92-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63e92-130">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="63e92-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63e92-131">입력</span><span class="sxs-lookup"><span data-stu-id="63e92-131">INPUTS</span></span>

### <span data-ttu-id="63e92-132">없음</span><span class="sxs-lookup"><span data-stu-id="63e92-132">None</span></span>

## <span data-ttu-id="63e92-133">출력</span><span class="sxs-lookup"><span data-stu-id="63e92-133">OUTPUTS</span></span>

### <span data-ttu-id="63e92-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="63e92-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="63e92-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="63e92-135">NOTES</span></span>

## <span data-ttu-id="63e92-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="63e92-136">RELATED LINKS</span></span>
