---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azdiagnosticsettingcategory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSettingCategory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSettingCategory.md
ms.openlocfilehash: 29c65ef5f5ec3b2b54fb883da706ddc9a38e1d4d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180177"
---
# <span data-ttu-id="4a64f-101">Get-AzDiagnosticSettingCategory</span><span class="sxs-lookup"><span data-stu-id="4a64f-101">Get-AzDiagnosticSettingCategory</span></span>

## <span data-ttu-id="4a64f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a64f-102">SYNOPSIS</span></span>
<span data-ttu-id="4a64f-103">Azure 리소스에 대해 지원되는 진단 설정 범주를 받거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="4a64f-103">Get or list supported diagnostic setting category for Azure resource.</span></span>

## <span data-ttu-id="4a64f-104">구문</span><span class="sxs-lookup"><span data-stu-id="4a64f-104">SYNTAX</span></span>

```
Get-AzDiagnosticSettingCategory -TargetResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a64f-105">설명</span><span class="sxs-lookup"><span data-stu-id="4a64f-105">DESCRIPTION</span></span>
<span data-ttu-id="4a64f-106">Azure 리소스에 대해 지원되는 진단 설정 범주를 받거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="4a64f-106">Get or list supported diagnostic setting category for Azure resource.</span></span>

## <span data-ttu-id="4a64f-107">예제</span><span class="sxs-lookup"><span data-stu-id="4a64f-107">EXAMPLES</span></span>

### <span data-ttu-id="4a64f-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="4a64f-108">Example 1</span></span>
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

<span data-ttu-id="4a64f-109">가상 네트워크에 대해 지원되는 진단 설정 범주를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="4a64f-109">Get supported diagnostic setting categories for virtual network.</span></span>

## <span data-ttu-id="4a64f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a64f-110">PARAMETERS</span></span>

### <span data-ttu-id="4a64f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a64f-111">-DefaultProfile</span></span>
<span data-ttu-id="4a64f-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4a64f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a64f-113">-Name</span><span class="sxs-lookup"><span data-stu-id="4a64f-113">-Name</span></span>
<span data-ttu-id="4a64f-114">진단 설정 범주의 이름</span><span class="sxs-lookup"><span data-stu-id="4a64f-114">Name of diagnostic setting category</span></span>

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

### <span data-ttu-id="4a64f-115">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="4a64f-115">-TargetResourceId</span></span>
<span data-ttu-id="4a64f-116">대상 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="4a64f-116">Target resource Id</span></span>

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

### <span data-ttu-id="4a64f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a64f-117">CommonParameters</span></span>
<span data-ttu-id="4a64f-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4a64f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a64f-119">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4a64f-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a64f-120">입력</span><span class="sxs-lookup"><span data-stu-id="4a64f-120">INPUTS</span></span>

### <span data-ttu-id="4a64f-121">System.String</span><span class="sxs-lookup"><span data-stu-id="4a64f-121">System.String</span></span>

## <span data-ttu-id="4a64f-122">출력</span><span class="sxs-lookup"><span data-stu-id="4a64f-122">OUTPUTS</span></span>

### <span data-ttu-id="4a64f-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticSettingCategory</span><span class="sxs-lookup"><span data-stu-id="4a64f-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticSettingCategory</span></span>

## <span data-ttu-id="4a64f-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4a64f-124">NOTES</span></span>

## <span data-ttu-id="4a64f-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4a64f-125">RELATED LINKS</span></span>
