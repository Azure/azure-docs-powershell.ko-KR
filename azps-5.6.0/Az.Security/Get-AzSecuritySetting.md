---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecuritySetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySetting.md
ms.openlocfilehash: 7c443625294b3a23ac79dfcbabb724a2d3fceaa3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971744"
---
# <span data-ttu-id="49c32-101">Get-AzSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="49c32-101">Get-AzSecuritySetting</span></span>

## <span data-ttu-id="49c32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49c32-102">SYNOPSIS</span></span>
<span data-ttu-id="49c32-103">Azure Security Center에서 보안 설정 사용</span><span class="sxs-lookup"><span data-stu-id="49c32-103">Get security settings in Azure Security Center</span></span>

## <span data-ttu-id="49c32-104">구문</span><span class="sxs-lookup"><span data-stu-id="49c32-104">SYNTAX</span></span>

### <span data-ttu-id="49c32-105">SubscriptionScope(기본값)</span><span class="sxs-lookup"><span data-stu-id="49c32-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49c32-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="49c32-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySetting -SettingName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49c32-107">설명</span><span class="sxs-lookup"><span data-stu-id="49c32-107">DESCRIPTION</span></span>
<span data-ttu-id="49c32-108">Get-AzSecuritySetting cmdlet은 Azure Security Center에서 보안 설정을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="49c32-108">The Get-AzSecuritySetting cmdlet get security settings in Azure Security Center.</span></span>

## <span data-ttu-id="49c32-109">예제</span><span class="sxs-lookup"><span data-stu-id="49c32-109">EXAMPLES</span></span>

### <span data-ttu-id="49c32-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="49c32-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSecuritySetting -SettingName "MCAS"

Id: "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/settings/MCAS"
Name: "MCAS"
Type: "Microsoft.Security/settings"
Enabled: true
```

<span data-ttu-id="49c32-111">MCAS 데이터 내보내기 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="49c32-111">Gets an MCAS data export setting</span></span>   

## <span data-ttu-id="49c32-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="49c32-112">PARAMETERS</span></span>

### <span data-ttu-id="49c32-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49c32-113">-DefaultProfile</span></span>
<span data-ttu-id="49c32-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="49c32-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49c32-115">-SettingName</span><span class="sxs-lookup"><span data-stu-id="49c32-115">-SettingName</span></span>
<span data-ttu-id="49c32-116">이름 설정.</span><span class="sxs-lookup"><span data-stu-id="49c32-116">Setting name.</span></span> <span data-ttu-id="49c32-117">(MCAS/WDATP)</span><span class="sxs-lookup"><span data-stu-id="49c32-117">(MCAS/WDATP)</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49c32-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49c32-118">CommonParameters</span></span>
<span data-ttu-id="49c32-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="49c32-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49c32-120">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49c32-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49c32-121">입력</span><span class="sxs-lookup"><span data-stu-id="49c32-121">INPUTS</span></span>

### <span data-ttu-id="49c32-122">System.String</span><span class="sxs-lookup"><span data-stu-id="49c32-122">System.String</span></span>

## <span data-ttu-id="49c32-123">출력</span><span class="sxs-lookup"><span data-stu-id="49c32-123">OUTPUTS</span></span>

### <span data-ttu-id="49c32-124">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="49c32-124">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="49c32-125">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="49c32-125">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

## <span data-ttu-id="49c32-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="49c32-126">NOTES</span></span>

## <span data-ttu-id="49c32-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="49c32-127">RELATED LINKS</span></span>
