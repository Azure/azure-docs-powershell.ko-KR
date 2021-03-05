---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azdiagnosticsettingcategory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSettingCategory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSettingCategory.md
ms.openlocfilehash: df263698a913faf361e5f23bb12d0267be314106
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980059"
---
# <span data-ttu-id="27ca9-101">Get-AzDiagnosticSettingCategory</span><span class="sxs-lookup"><span data-stu-id="27ca9-101">Get-AzDiagnosticSettingCategory</span></span>

## <span data-ttu-id="27ca9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27ca9-102">SYNOPSIS</span></span>
<span data-ttu-id="27ca9-103">Azure 리소스에 대해 지원되는 진단 설정 범주를 얻거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="27ca9-103">Get or list supported diagnostic setting category for Azure resource.</span></span>

## <span data-ttu-id="27ca9-104">구문</span><span class="sxs-lookup"><span data-stu-id="27ca9-104">SYNTAX</span></span>

```
Get-AzDiagnosticSettingCategory -TargetResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27ca9-105">설명</span><span class="sxs-lookup"><span data-stu-id="27ca9-105">DESCRIPTION</span></span>
<span data-ttu-id="27ca9-106">Azure 리소스에 대해 지원되는 진단 설정 범주를 얻거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="27ca9-106">Get or list supported diagnostic setting category for Azure resource.</span></span>

## <span data-ttu-id="27ca9-107">예제</span><span class="sxs-lookup"><span data-stu-id="27ca9-107">EXAMPLES</span></span>

### <span data-ttu-id="27ca9-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="27ca9-108">Example 1</span></span>
```powershell
PS C:\> Get-AzDiagnosticSettingCategory -TargetResourceId /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX
Id           : /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX/providers/microsoft.insights/diagnosticSettingsCategories/VMProtectionAlerts
Name         : VMProtectionAlerts
Type         : microsoft.insights/diagnosticSettingsCategories
CategoryType : Logs

Id           : /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX/providers/microsoft.insights/diagnosticSettingsCategories/AllMetrics
Name         : AllMetrics
Type         : microsoft.insights/diagnosticSettingsCategories
CategoryType : Metrics
```

<span data-ttu-id="27ca9-109">가상 네트워크에 대한 지원되는 진단 설정 범주를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="27ca9-109">Get supported diagnostic setting categories for virtual network.</span></span>

## <span data-ttu-id="27ca9-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="27ca9-110">PARAMETERS</span></span>

### <span data-ttu-id="27ca9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27ca9-111">-DefaultProfile</span></span>
<span data-ttu-id="27ca9-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="27ca9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27ca9-113">-Name</span><span class="sxs-lookup"><span data-stu-id="27ca9-113">-Name</span></span>
<span data-ttu-id="27ca9-114">진단 설정 범주의 이름</span><span class="sxs-lookup"><span data-stu-id="27ca9-114">Name of diagnostic setting category</span></span>

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

### <span data-ttu-id="27ca9-115">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="27ca9-115">-TargetResourceId</span></span>
<span data-ttu-id="27ca9-116">대상 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="27ca9-116">Target resource Id</span></span>

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

### <span data-ttu-id="27ca9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27ca9-117">CommonParameters</span></span>
<span data-ttu-id="27ca9-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="27ca9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27ca9-119">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="27ca9-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27ca9-120">입력</span><span class="sxs-lookup"><span data-stu-id="27ca9-120">INPUTS</span></span>

### <span data-ttu-id="27ca9-121">System.String</span><span class="sxs-lookup"><span data-stu-id="27ca9-121">System.String</span></span>

## <span data-ttu-id="27ca9-122">출력</span><span class="sxs-lookup"><span data-stu-id="27ca9-122">OUTPUTS</span></span>

### <span data-ttu-id="27ca9-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticSettingCategory</span><span class="sxs-lookup"><span data-stu-id="27ca9-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticSettingCategory</span></span>

## <span data-ttu-id="27ca9-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="27ca9-124">NOTES</span></span>

## <span data-ttu-id="27ca9-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="27ca9-125">RELATED LINKS</span></span>
