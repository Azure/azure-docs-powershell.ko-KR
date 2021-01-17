---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzConfigurationAssignment.md
ms.openlocfilehash: 20ca0e52b23ddcabfe14b2bd2fc9ab633f225390
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332565"
---
# <span data-ttu-id="36cfa-101">Get-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="36cfa-101">Get-AzConfigurationAssignment</span></span>

## <span data-ttu-id="36cfa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36cfa-102">SYNOPSIS</span></span>
<span data-ttu-id="36cfa-103">리소스에 대한 configurationAssignments를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="36cfa-103">List configurationAssignments for resource.</span></span>

## <span data-ttu-id="36cfa-104">구문</span><span class="sxs-lookup"><span data-stu-id="36cfa-104">SYNTAX</span></span>

```
Get-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36cfa-105">설명</span><span class="sxs-lookup"><span data-stu-id="36cfa-105">DESCRIPTION</span></span>
<span data-ttu-id="36cfa-106">리소스에 대한 configurationAssignments를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="36cfa-106">List configurationAssignments for resource.</span></span>

## <span data-ttu-id="36cfa-107">예제</span><span class="sxs-lookup"><span data-stu-id="36cfa-107">EXAMPLES</span></span>

### <span data-ttu-id="36cfa-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="36cfa-108">Example 1</span></span>
```powershell
PS C:\> Get-AzConfigurationAssignment -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute


MaintenanceConfigurationId : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/ps1/providers/Microsoft.Maintenance/maintenanceConfigurations/ps2
Id                         :
/subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/configurationAssignments/ps2
Name                       : ps2
Type                       : Microsoft.Maintenance/configurationAssignments
```

<span data-ttu-id="36cfa-109">전용 호스트에 대한 configurationAssignments를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="36cfa-109">List configurationAssignments for dedicated host.</span></span>

## <span data-ttu-id="36cfa-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36cfa-110">PARAMETERS</span></span>

### <span data-ttu-id="36cfa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36cfa-111">-DefaultProfile</span></span>
<span data-ttu-id="36cfa-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="36cfa-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36cfa-113">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="36cfa-113">-ProviderName</span></span>
<span data-ttu-id="36cfa-114">리소스 공급자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="36cfa-114">The resource provider Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36cfa-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36cfa-115">-ResourceGroupName</span></span>
<span data-ttu-id="36cfa-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="36cfa-116">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36cfa-117">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="36cfa-117">-ResourceName</span></span>
<span data-ttu-id="36cfa-118">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="36cfa-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36cfa-119">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="36cfa-119">-ResourceParentName</span></span>
<span data-ttu-id="36cfa-120">부모 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="36cfa-120">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36cfa-121">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="36cfa-121">-ResourceParentType</span></span>
<span data-ttu-id="36cfa-122">부모 리소스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="36cfa-122">The parent resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36cfa-123">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="36cfa-123">-ResourceType</span></span>
<span data-ttu-id="36cfa-124">리소스 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="36cfa-124">The resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36cfa-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36cfa-125">CommonParameters</span></span>
<span data-ttu-id="36cfa-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="36cfa-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36cfa-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="36cfa-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36cfa-128">입력</span><span class="sxs-lookup"><span data-stu-id="36cfa-128">INPUTS</span></span>

### <span data-ttu-id="36cfa-129">System.String</span><span class="sxs-lookup"><span data-stu-id="36cfa-129">System.String</span></span>

## <span data-ttu-id="36cfa-130">출력</span><span class="sxs-lookup"><span data-stu-id="36cfa-130">OUTPUTS</span></span>

### <span data-ttu-id="36cfa-131">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="36cfa-131">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span></span>

## <span data-ttu-id="36cfa-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="36cfa-132">NOTES</span></span>

## <span data-ttu-id="36cfa-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="36cfa-133">RELATED LINKS</span></span>
