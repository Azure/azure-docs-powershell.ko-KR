---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzIotSecurityAnalytics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalytics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalytics.md
ms.openlocfilehash: 56827f5a461239ceae756591b82ff687cb50053c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308693"
---
# <span data-ttu-id="e964c-101">Get-AzIotSecurityAnalytics</span><span class="sxs-lookup"><span data-stu-id="e964c-101">Get-AzIotSecurityAnalytics</span></span>

## <span data-ttu-id="e964c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e964c-102">SYNOPSIS</span></span>
<span data-ttu-id="e964c-103">IoT security 분석 가져오기</span><span class="sxs-lookup"><span data-stu-id="e964c-103">Get IoT security analytics</span></span>

## <span data-ttu-id="e964c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e964c-104">SYNTAX</span></span>

```
Get-AzIotSecurityAnalytics -ResourceGroupName <String> -SolutionName <String> [-Default]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e964c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e964c-105">DESCRIPTION</span></span>
<span data-ttu-id="e964c-106">Get-AzIotSecurityAnalytics cmdlet은 특정 iot security 솔루션의 보안 분석 집합을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e964c-106">The Get-AzIotSecurityAnalytics cmdlet returns a set of security analytics of a specific iot security solution</span></span>

## <span data-ttu-id="e964c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e964c-107">EXAMPLES</span></span>

### <span data-ttu-id="e964c-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="e964c-108">Example 1</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalytics -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution" -Default

Id: "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolution/analyticsModels/default"
Name: "default"
Type: "Microsoft.Security/IoTSecuritySolutionAnalyticsModel"
Metrics: {
            High": 5
            Medium: 200
            Low: 102
          }
UnhealthyDeviceCount: 1200
DevicesMetrics: [
            {
              Date: "2019-02-01T00:00:00Z"
              DevicesMetrics: {
                High: 3
                Medium: 15
                Low: 70
              }
            }
            {
              Date: "2019-02-02T00:00:00Z"
              DevicesMetrics: {
                High: 3
                Medium: 45
                Low: 65
              }
            }
          ]
TopAlertedDevices: [
            {
              DeviceId: "id1"
              AlertsCount: 200
            }
            {
              DeviceId": "id2"
              AlertsCount": 170
            }
            {
              DeviceId": "id3"
              AlertsCount": 150
            }
          ]
MostPrevalentDeviceAlerts: [
            {
              AlertDisplayName: "Custom Alert - number of device to cloud messages in AMQP protocol is not in the allowed range"
              ReportedSeverity: "Low"
              AlertsCount: 200
            }
            {
              AlertDisplayName: "Custom Alert - execution of a process that is not allowed"
              ReportedSeverity: "Medium"
              AlertsCount: 170
            }
            {
              AlertDisplayName": "Successful Bruteforce"
              ReportedSeverity": "Low"
              AlertsCount": 150
            }
          ]
MostPrevalentDeviceRecommendations: [
            {
              RecommendationDisplayName: "Install the Azure Security of Things Agent"
              ReportedSeverity: "Low"
              DevicesCount: 200
            }
            {
              RecommendationDisplayName: "High level permissions configured in Edge model twin for Edge module"
              ReportedSeverity: "Low"
              DevicesCount: 170
            }
            {
              RrecommendationDisplayName: "Same Authentication Credentials used by multiple devices"
              ReportedSeverity: "Medium"
              DevicesCount: 150
            }
          ]
        }
      }
```

<span data-ttu-id="e964c-109">Reasource 그룹 "Mysolution"에서 보안 솔루션 "MySolution"에 대 한 deafult IoT 보안 분석 가져오기</span><span class="sxs-lookup"><span data-stu-id="e964c-109">Get the deafult IoT Security Analytics for Security Solution "MySolution" in reasource group "MyResourceGroup"</span></span>

## <span data-ttu-id="e964c-110">변수</span><span class="sxs-lookup"><span data-stu-id="e964c-110">PARAMETERS</span></span>

### <span data-ttu-id="e964c-111">-기본</span><span class="sxs-lookup"><span data-stu-id="e964c-111">-Default</span></span>
<span data-ttu-id="e964c-112">기본 분석 집합을 가져오고, 그렇지 않으면 모든 분석 집합 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e964c-112">If present, get the default analytics set, otherwise, get the list of all analytics sets.</span></span>

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

### <span data-ttu-id="e964c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e964c-113">-DefaultProfile</span></span>
<span data-ttu-id="e964c-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e964c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e964c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e964c-115">-ResourceGroupName</span></span>
<span data-ttu-id="e964c-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e964c-116">Resource group name.</span></span>

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

### <span data-ttu-id="e964c-117">-SolutionName</span><span class="sxs-lookup"><span data-stu-id="e964c-117">-SolutionName</span></span>
<span data-ttu-id="e964c-118">솔루션 이름</span><span class="sxs-lookup"><span data-stu-id="e964c-118">Solution name</span></span>

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

### <span data-ttu-id="e964c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e964c-119">CommonParameters</span></span>
<span data-ttu-id="e964c-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e964c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e964c-121">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e964c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e964c-122">입력</span><span class="sxs-lookup"><span data-stu-id="e964c-122">INPUTS</span></span>

### <span data-ttu-id="e964c-123">않아야</span><span class="sxs-lookup"><span data-stu-id="e964c-123">None</span></span>

## <span data-ttu-id="e964c-124">출력</span><span class="sxs-lookup"><span data-stu-id="e964c-124">OUTPUTS</span></span>

### <span data-ttu-id="e964c-125">Microsoft. Azure. i. i a m. i a m.</span><span class="sxs-lookup"><span data-stu-id="e964c-125">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIotSecuritySolutionAnalytics</span></span>

## <span data-ttu-id="e964c-126">상속자</span><span class="sxs-lookup"><span data-stu-id="e964c-126">NOTES</span></span>

## <span data-ttu-id="e964c-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e964c-127">RELATED LINKS</span></span>
