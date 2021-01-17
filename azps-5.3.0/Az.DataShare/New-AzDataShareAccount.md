---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareAccount.md
ms.openlocfilehash: b24fe9e6587fe50a41d601c70c2687891bea2f16
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377252"
---
# <span data-ttu-id="daa71-101">New-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="daa71-101">New-AzDataShareAccount</span></span>

## <span data-ttu-id="daa71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="daa71-102">SYNOPSIS</span></span>
<span data-ttu-id="daa71-103">새 데이터 공유 계정 생성</span><span class="sxs-lookup"><span data-stu-id="daa71-103">Creates new data share account</span></span>

## <span data-ttu-id="daa71-104">구문</span><span class="sxs-lookup"><span data-stu-id="daa71-104">SYNTAX</span></span>

```
New-AzDataShareAccount -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="daa71-105">설명</span><span class="sxs-lookup"><span data-stu-id="daa71-105">DESCRIPTION</span></span>
<span data-ttu-id="daa71-106">**New-AzDataShareAccount** cmdlet은 지정된 Azure 리소스 그룹에 데이터 공유 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="daa71-106">**New-AzDataShareAccount** cmdlet creates a datashare account in the specified Azure resource group.</span></span>

## <span data-ttu-id="daa71-107">예제</span><span class="sxs-lookup"><span data-stu-id="daa71-107">EXAMPLES</span></span>

### <span data-ttu-id="daa71-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="daa71-108">Example 1</span></span>
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

<span data-ttu-id="daa71-109">리소스 그룹 "ADS"에서 "WikiADS"라는 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="daa71-109">Creates an account named "WikiADS" in resource group "ADS"</span></span>

## <span data-ttu-id="daa71-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="daa71-110">PARAMETERS</span></span>

### <span data-ttu-id="daa71-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="daa71-111">-AsJob</span></span>
<span data-ttu-id="daa71-112">{{AsJob 설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="daa71-112">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="daa71-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daa71-113">-DefaultProfile</span></span>
<span data-ttu-id="daa71-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="daa71-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="daa71-115">-Location</span><span class="sxs-lookup"><span data-stu-id="daa71-115">-Location</span></span>
<span data-ttu-id="daa71-116">데이터 공유 계정을 만들 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="daa71-116">The location in which to create the data share account.</span></span>

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

### <span data-ttu-id="daa71-117">-Name</span><span class="sxs-lookup"><span data-stu-id="daa71-117">-Name</span></span>
<span data-ttu-id="daa71-118">Azure 데이터 공유 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="daa71-118">Azure data share account name.</span></span>

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

### <span data-ttu-id="daa71-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="daa71-119">-ResourceGroupName</span></span>
<span data-ttu-id="daa71-120">Azure 데이터 공유 계정의 리소스 그룹 이름이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="daa71-120">The resource group name of the azure data share account will be created in.</span></span>

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

### <span data-ttu-id="daa71-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="daa71-121">-Tag</span></span>
<span data-ttu-id="daa71-122">Azure 데이터 공유 계정과 연결하기 위해 사용할 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="daa71-122">The tags to associate with the azure data share account.</span></span>

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

### <span data-ttu-id="daa71-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="daa71-123">-Confirm</span></span>
<span data-ttu-id="daa71-124">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="daa71-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="daa71-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="daa71-125">-WhatIf</span></span>
<span data-ttu-id="daa71-126">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="daa71-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="daa71-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="daa71-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="daa71-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daa71-128">CommonParameters</span></span>
<span data-ttu-id="daa71-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="daa71-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daa71-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="daa71-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daa71-131">입력</span><span class="sxs-lookup"><span data-stu-id="daa71-131">INPUTS</span></span>

### <span data-ttu-id="daa71-132">없음</span><span class="sxs-lookup"><span data-stu-id="daa71-132">None</span></span>

## <span data-ttu-id="daa71-133">출력</span><span class="sxs-lookup"><span data-stu-id="daa71-133">OUTPUTS</span></span>

### <span data-ttu-id="daa71-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="daa71-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="daa71-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="daa71-135">NOTES</span></span>

## <span data-ttu-id="daa71-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="daa71-136">RELATED LINKS</span></span>
