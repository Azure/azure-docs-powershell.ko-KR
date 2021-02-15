---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySetting.md
ms.openlocfilehash: 708fb6b3807e874d00c3e555ef84973572edcd1c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189137"
---
# <span data-ttu-id="741b6-101">Get-AzSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="741b6-101">Get-AzSecuritySetting</span></span>

## <span data-ttu-id="741b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="741b6-102">SYNOPSIS</span></span>
<span data-ttu-id="741b6-103">Azure Security Center에서 보안 설정 사용</span><span class="sxs-lookup"><span data-stu-id="741b6-103">Get security settings in Azure Security Center</span></span>

## <span data-ttu-id="741b6-104">구문</span><span class="sxs-lookup"><span data-stu-id="741b6-104">SYNTAX</span></span>

### <span data-ttu-id="741b6-105">SubscriptionScope(기본값)</span><span class="sxs-lookup"><span data-stu-id="741b6-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="741b6-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="741b6-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySetting -SettingName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="741b6-107">설명</span><span class="sxs-lookup"><span data-stu-id="741b6-107">DESCRIPTION</span></span>
<span data-ttu-id="741b6-108">이 Get-AzSecuritySetting cmdlet은 Azure Security Center에서 보안 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="741b6-108">The Get-AzSecuritySetting cmdlet get security settings in Azure Security Center.</span></span>

## <span data-ttu-id="741b6-109">예제</span><span class="sxs-lookup"><span data-stu-id="741b6-109">EXAMPLES</span></span>

### <span data-ttu-id="741b6-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="741b6-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSecuritySetting -SettingName "MCAS"

Id: "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/settings/MCAS"
Name: "MCAS"
Type: "Microsoft.Security/settings"
Enabled: true
```

<span data-ttu-id="741b6-111">MCAS 데이터 내보내기 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="741b6-111">Gets an MCAS data export setting</span></span>   

## <span data-ttu-id="741b6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="741b6-112">PARAMETERS</span></span>

### <span data-ttu-id="741b6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="741b6-113">-DefaultProfile</span></span>
<span data-ttu-id="741b6-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="741b6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="741b6-115">-SettingName</span><span class="sxs-lookup"><span data-stu-id="741b6-115">-SettingName</span></span>
<span data-ttu-id="741b6-116">설정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="741b6-116">Setting name.</span></span> <span data-ttu-id="741b6-117">(MCAS/WDATP)</span><span class="sxs-lookup"><span data-stu-id="741b6-117">(MCAS/WDATP)</span></span>

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

### <span data-ttu-id="741b6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="741b6-118">CommonParameters</span></span>
<span data-ttu-id="741b6-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="741b6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="741b6-120">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="741b6-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="741b6-121">입력</span><span class="sxs-lookup"><span data-stu-id="741b6-121">INPUTS</span></span>

### <span data-ttu-id="741b6-122">System.String</span><span class="sxs-lookup"><span data-stu-id="741b6-122">System.String</span></span>

## <span data-ttu-id="741b6-123">출력</span><span class="sxs-lookup"><span data-stu-id="741b6-123">OUTPUTS</span></span>

### <span data-ttu-id="741b6-124">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="741b6-124">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="741b6-125">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="741b6-125">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

## <span data-ttu-id="741b6-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="741b6-126">NOTES</span></span>

## <span data-ttu-id="741b6-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="741b6-127">RELATED LINKS</span></span>
