---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/powershell/module/az.maintenance/get-azmaintenancepublicconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenancePublicConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenancePublicConfiguration.md
ms.openlocfilehash: a4625d48086064fb59b5f2faee78357380f6a323
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001243"
---
# <span data-ttu-id="4a630-101">Get-AzMaintenancePublicConfiguration</span><span class="sxs-lookup"><span data-stu-id="4a630-101">Get-AzMaintenancePublicConfiguration</span></span>

## <span data-ttu-id="4a630-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a630-102">SYNOPSIS</span></span>
<span data-ttu-id="4a630-103">공용 유지 관리 구성 레코드를 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4a630-103">Get Public Maintenance Configuration record</span></span>

## <span data-ttu-id="4a630-104">구문</span><span class="sxs-lookup"><span data-stu-id="4a630-104">SYNTAX</span></span>

```
Get-AzMaintenancePublicConfiguration [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a630-105">설명</span><span class="sxs-lookup"><span data-stu-id="4a630-105">DESCRIPTION</span></span>
<span data-ttu-id="4a630-106">공용 유지 관리 구성 레코드를 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4a630-106">Get Public Maintenance Configuration record</span></span>

## <span data-ttu-id="4a630-107">예제</span><span class="sxs-lookup"><span data-stu-id="4a630-107">EXAMPLES</span></span>

### <span data-ttu-id="4a630-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="4a630-108">Example 1</span></span>
```powershell
PS C:\> Get-AzMaintenancePublicConfiguration -ResourceGroupName smdtest -Name workervmscentralus


Location            : centralus
Tags                : {}
NamespaceProperty   :
ExtensionProperties : {"publicMaintenanceConfigurationId" : "workervmscentralus"}
StartDateTime       : 2020-08-01 00:00
ExpirationDateTime  : 2021-08-04 00:00
TimeZone            : Pacific Standard Time
RecurEvery          : Day
Duration            : 05:00
MaintenanceScope    : SQLDB
Visibility          : Public
Id                  : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtest/providers/Microsoft.Maintenance/publicMaintenanceConfigurations/workervmscentralus
Name                : workervmscentralus
Type                : Microsoft.Maintenance/publicMaintenanceConfigurations
```

<span data-ttu-id="4a630-109">공용 유지 관리 구성 레코드를 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4a630-109">Get Public Maintenance configuration record</span></span>

## <span data-ttu-id="4a630-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="4a630-110">PARAMETERS</span></span>

### <span data-ttu-id="4a630-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a630-111">-DefaultProfile</span></span>
<span data-ttu-id="4a630-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4a630-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a630-113">-Name</span><span class="sxs-lookup"><span data-stu-id="4a630-113">-Name</span></span>
<span data-ttu-id="4a630-114">공용 유지 관리 구성 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4a630-114">The public maintenance configuration Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a630-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a630-115">-ResourceGroupName</span></span>
<span data-ttu-id="4a630-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4a630-116">The resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a630-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a630-117">CommonParameters</span></span>
<span data-ttu-id="4a630-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4a630-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a630-119">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4a630-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a630-120">입력</span><span class="sxs-lookup"><span data-stu-id="4a630-120">INPUTS</span></span>

### <span data-ttu-id="4a630-121">System.String</span><span class="sxs-lookup"><span data-stu-id="4a630-121">System.String</span></span>

## <span data-ttu-id="4a630-122">출력</span><span class="sxs-lookup"><span data-stu-id="4a630-122">OUTPUTS</span></span>

### <span data-ttu-id="4a630-123">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="4a630-123">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="4a630-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4a630-124">NOTES</span></span>

## <span data-ttu-id="4a630-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4a630-125">RELATED LINKS</span></span>
