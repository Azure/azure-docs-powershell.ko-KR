---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppTrafficRouting.md
ms.openlocfilehash: 0dda79130d150265d8050fcb5ba951cd243bebda
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491429"
---
# <span data-ttu-id="bbf04-101">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="bbf04-101">Remove-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="bbf04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bbf04-102">SYNOPSIS</span></span>
<span data-ttu-id="bbf04-103">슬롯에서 라우팅 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="bbf04-103">Remove a routing Rule from the Slot.</span></span>

## <span data-ttu-id="bbf04-104">구문</span><span class="sxs-lookup"><span data-stu-id="bbf04-104">SYNTAX</span></span>

```
Remove-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RuleName <String>
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbf04-105">설명</span><span class="sxs-lookup"><span data-stu-id="bbf04-105">DESCRIPTION</span></span>
<span data-ttu-id="bbf04-106">**Remove-AzWebAppTrafficRouting** cmdlet은 Azure 웹앱 슬롯에서 라우팅 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="bbf04-106">The **Remove-AzWebAppTrafficRouting** cmdlet removes a routing rule from an Azure Web App Slot.</span></span>

## <span data-ttu-id="bbf04-107">예제</span><span class="sxs-lookup"><span data-stu-id="bbf04-107">EXAMPLES</span></span>

### <span data-ttu-id="bbf04-108">예제 1 웹앱 슬롯에서 특정 라우팅 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="bbf04-108">Example 1 Removes the specific routing rule from webapp slot</span></span>
```powershell
PS C:\> Remove-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite"  -RuleName 'Stg'
```

<span data-ttu-id="bbf04-109">이 명령은 주어진 웹앱 슬롯에 대한 라우팅 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="bbf04-109">This command removes a routing rule for a given webapp slot.</span></span>

## <span data-ttu-id="bbf04-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bbf04-110">PARAMETERS</span></span>

### <span data-ttu-id="bbf04-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbf04-111">-DefaultProfile</span></span>
<span data-ttu-id="bbf04-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bbf04-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbf04-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbf04-113">-ResourceGroupName</span></span>
<span data-ttu-id="bbf04-114">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="bbf04-114">Resource Group Name</span></span>

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

### <span data-ttu-id="bbf04-115">-RuleName</span><span class="sxs-lookup"><span data-stu-id="bbf04-115">-RuleName</span></span>
<span data-ttu-id="bbf04-116">규칙 이름</span><span class="sxs-lookup"><span data-stu-id="bbf04-116">Rule Name</span></span>

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

### <span data-ttu-id="bbf04-117">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="bbf04-117">-WebAppName</span></span>
<span data-ttu-id="bbf04-118">WebApp 이름</span><span class="sxs-lookup"><span data-stu-id="bbf04-118">WebApp Name</span></span>

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

### <span data-ttu-id="bbf04-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bbf04-119">-PassThru</span></span>
<span data-ttu-id="bbf04-120">액세스 제한 구성 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="bbf04-120">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="bbf04-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bbf04-121">-Confirm</span></span>
<span data-ttu-id="bbf04-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bbf04-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbf04-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbf04-123">-WhatIf</span></span>
<span data-ttu-id="bbf04-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="bbf04-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbf04-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bbf04-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbf04-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbf04-126">CommonParameters</span></span>
<span data-ttu-id="bbf04-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bbf04-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbf04-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bbf04-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbf04-129">입력</span><span class="sxs-lookup"><span data-stu-id="bbf04-129">INPUTS</span></span>

### <span data-ttu-id="bbf04-130">없음</span><span class="sxs-lookup"><span data-stu-id="bbf04-130">None</span></span>

## <span data-ttu-id="bbf04-131">출력</span><span class="sxs-lookup"><span data-stu-id="bbf04-131">OUTPUTS</span></span>

### <span data-ttu-id="bbf04-132">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span><span class="sxs-lookup"><span data-stu-id="bbf04-132">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="bbf04-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bbf04-133">NOTES</span></span>

## <span data-ttu-id="bbf04-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bbf04-134">RELATED LINKS</span></span>
[<span data-ttu-id="bbf04-135">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="bbf04-135">Add-AzWebAppTrafficRouting</span></span>](./Add-AzWebAppTrafficRouting.md)

[<span data-ttu-id="bbf04-136">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="bbf04-136">Get-AzWebAppTrafficRouting</span></span>](./Get-AzWebAppTrafficRouting.md)

[<span data-ttu-id="bbf04-137">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="bbf04-137">Update-AzWebAppTrafficRouting</span></span>](./Update-AzWebAppTrafficRouting.md)