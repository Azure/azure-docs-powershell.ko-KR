---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/remove-azmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Remove-AzMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Remove-AzMapsAccount.md
ms.openlocfilehash: b84a5d6cbbf090243a63ad9919a3fbb1977d77f5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492284"
---
# <span data-ttu-id="9d1a1-101">Remove-AzMapsAccount</span><span class="sxs-lookup"><span data-stu-id="9d1a1-101">Remove-AzMapsAccount</span></span>

## <span data-ttu-id="9d1a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d1a1-102">SYNOPSIS</span></span>
<span data-ttu-id="9d1a1-103">Azure Maps 계정을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="9d1a1-103">Deletes an Azure Maps account.</span></span>

## <span data-ttu-id="9d1a1-104">구문</span><span class="sxs-lookup"><span data-stu-id="9d1a1-104">SYNTAX</span></span>

### <span data-ttu-id="9d1a1-105">NameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="9d1a1-105">NameParameterSet (Default)</span></span>
```
Remove-AzMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d1a1-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d1a1-106">InputObjectParameterSet</span></span>
```
Remove-AzMapsAccount [-InputObject <PSMapsAccount>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d1a1-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d1a1-107">ResourceIdParameterSet</span></span>
```
Remove-AzMapsAccount [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d1a1-108">설명</span><span class="sxs-lookup"><span data-stu-id="9d1a1-108">DESCRIPTION</span></span>
<span data-ttu-id="9d1a1-109">이 Remove-AzMapsAccount cmdlet은 지정된 Azure Maps 계정을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="9d1a1-109">The Remove-AzMapsAccount cmdlet deletes the specified Azure Maps account.</span></span>

## <span data-ttu-id="9d1a1-110">예제</span><span class="sxs-lookup"><span data-stu-id="9d1a1-110">EXAMPLES</span></span>

### <span data-ttu-id="9d1a1-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="9d1a1-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="9d1a1-112">리소스 그룹 MyResourceGroup에서 MyAccount 계정을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="9d1a1-112">Deletes the account MyAccount from the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="9d1a1-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="9d1a1-113">Example 2</span></span>
```
PS C:\> Remove-AzMapsAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="9d1a1-114">지정된 Azure Maps 계정을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="9d1a1-114">Deletes the specified Azure Maps Account.</span></span>

## <span data-ttu-id="9d1a1-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d1a1-115">PARAMETERS</span></span>

### <span data-ttu-id="9d1a1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d1a1-116">-DefaultProfile</span></span>
<span data-ttu-id="9d1a1-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9d1a1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d1a1-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9d1a1-118">-InputObject</span></span>
<span data-ttu-id="9d1a1-119">Get-AzMapsAccount에서 파이프된 Maps 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="9d1a1-119">Maps Account piped from Get-AzMapsAccount.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Maps.Models.PSMapsAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d1a1-120">-Name</span><span class="sxs-lookup"><span data-stu-id="9d1a1-120">-Name</span></span>
<span data-ttu-id="9d1a1-121">계정 이름을 매핑합니다.</span><span class="sxs-lookup"><span data-stu-id="9d1a1-121">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d1a1-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9d1a1-122">-PassThru</span></span>
<span data-ttu-id="9d1a1-123">지정된 계정이 성공적으로 삭제됐는지 여부를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="9d1a1-123">Return whether the specified account was successfully deleted or not.</span></span>

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

### <span data-ttu-id="9d1a1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d1a1-124">-ResourceGroupName</span></span>
<span data-ttu-id="9d1a1-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9d1a1-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d1a1-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9d1a1-126">-ResourceId</span></span>
<span data-ttu-id="9d1a1-127">계정 ResourceId를 매핑합니다.</span><span class="sxs-lookup"><span data-stu-id="9d1a1-127">Maps Account ResourceId.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d1a1-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9d1a1-128">-Confirm</span></span>
<span data-ttu-id="9d1a1-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9d1a1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d1a1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d1a1-130">-WhatIf</span></span>
<span data-ttu-id="9d1a1-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="9d1a1-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d1a1-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9d1a1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d1a1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d1a1-133">CommonParameters</span></span>
<span data-ttu-id="9d1a1-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9d1a1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d1a1-135">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9d1a1-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d1a1-136">입력</span><span class="sxs-lookup"><span data-stu-id="9d1a1-136">INPUTS</span></span>

### <span data-ttu-id="9d1a1-137">System.String</span><span class="sxs-lookup"><span data-stu-id="9d1a1-137">System.String</span></span>

### <span data-ttu-id="9d1a1-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="9d1a1-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="9d1a1-139">출력</span><span class="sxs-lookup"><span data-stu-id="9d1a1-139">OUTPUTS</span></span>

### <span data-ttu-id="9d1a1-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9d1a1-140">System.Boolean</span></span>

## <span data-ttu-id="9d1a1-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9d1a1-141">NOTES</span></span>

## <span data-ttu-id="9d1a1-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9d1a1-142">RELATED LINKS</span></span>
