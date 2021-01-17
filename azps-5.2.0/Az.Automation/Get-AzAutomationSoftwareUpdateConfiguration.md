---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: af11442edfc5acb2d7e9683bc71d7d2e2c87bd5f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373731"
---
# <span data-ttu-id="b60cf-101">Get-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="b60cf-101">Get-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="b60cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b60cf-102">SYNOPSIS</span></span>
<span data-ttu-id="b60cf-103">Azure Automation 소프트웨어 업데이트 구성 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b60cf-103">Gets a list of azure automation software update configurations.</span></span>

## <span data-ttu-id="b60cf-104">구문</span><span class="sxs-lookup"><span data-stu-id="b60cf-104">SYNTAX</span></span>

### <span data-ttu-id="b60cf-105">ByAll(기본값)</span><span class="sxs-lookup"><span data-stu-id="b60cf-105">ByAll (Default)</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b60cf-106">ByName</span><span class="sxs-lookup"><span data-stu-id="b60cf-106">ByName</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b60cf-107">ByVMId</span><span class="sxs-lookup"><span data-stu-id="b60cf-107">ByVMId</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration -AzureVMResourceId <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b60cf-108">설명</span><span class="sxs-lookup"><span data-stu-id="b60cf-108">DESCRIPTION</span></span>
<span data-ttu-id="b60cf-109">이 Get-AzAutomationSoftwareUpdateConfiguration 소프트웨어 업데이트 구성 목록을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="b60cf-109">The Get-AzAutomationSoftwareUpdateConfiguration returns a list of software update configurations.</span></span> <span data-ttu-id="b60cf-110">특정 소프트웨어 업데이트 구성을 얻습니다. 이름 매개 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b60cf-110">To get a specific software update configuration, specify the name parameter.</span></span> <span data-ttu-id="b60cf-111">이 가상 머신에 대한 Azure 리소스 ID를 지정하여 특정 Azure 가상 머신을 대상으로 하는 소프트웨어 업데이트 구성을 나열할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b60cf-111">You can also list software update configurations targeting specific azure virtual machine by specifying the azure resource Id for this virtual machine.</span></span>

## <span data-ttu-id="b60cf-112">예제</span><span class="sxs-lookup"><span data-stu-id="b60cf-112">EXAMPLES</span></span>

### <span data-ttu-id="b60cf-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="b60cf-113">Example 1</span></span>
<span data-ttu-id="b60cf-114">이름으로 Azure Automation 소프트웨어 업데이트 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b60cf-114">Get an azure automation software update configuration by name.</span></span>

```powershell
PS C:\> Get-AzAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" -AutomationAccountName "myaccount" -Name "MyWeeklySchedule"

UpdateConfiguration   : Microsoft.Azure.Commands.Automation.Model.UpdateManagement.UpdateConfiguration
ScheduleConfiguration : Microsoft.Azure.Commands.Automation.Model.Schedule
ProvisioningState     : Succeeded
ErrorInfo             :
ResourceGroupName     : mygroup
AutomationAccountName : myaccount
Name                  : MyWeeklySchedule
CreationTime          : 9/14/2018 3:53:27 AM +00:00
LastModifiedTime      : 9/14/2018 3:53:37 AM +00:00
Description           :
```

## <span data-ttu-id="b60cf-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b60cf-115">PARAMETERS</span></span>

### <span data-ttu-id="b60cf-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b60cf-116">-AutomationAccountName</span></span>
<span data-ttu-id="b60cf-117">자동화 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b60cf-117">The automation account name.</span></span>

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

### <span data-ttu-id="b60cf-118">-AzureVMResourceId</span><span class="sxs-lookup"><span data-stu-id="b60cf-118">-AzureVMResourceId</span></span>
<span data-ttu-id="b60cf-119">가상 머신의 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b60cf-119">Azure resource Id of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVMId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b60cf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b60cf-120">-DefaultProfile</span></span>
<span data-ttu-id="b60cf-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b60cf-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b60cf-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b60cf-122">-Name</span></span>
<span data-ttu-id="b60cf-123">소프트웨어 업데이트 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b60cf-123">Name of the software update configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b60cf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b60cf-124">-ResourceGroupName</span></span>
<span data-ttu-id="b60cf-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b60cf-125">The resource group name.</span></span>

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

### <span data-ttu-id="b60cf-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b60cf-126">CommonParameters</span></span>
<span data-ttu-id="b60cf-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b60cf-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b60cf-128">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b60cf-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b60cf-129">입력</span><span class="sxs-lookup"><span data-stu-id="b60cf-129">INPUTS</span></span>

### <span data-ttu-id="b60cf-130">System.String</span><span class="sxs-lookup"><span data-stu-id="b60cf-130">System.String</span></span>

## <span data-ttu-id="b60cf-131">출력</span><span class="sxs-lookup"><span data-stu-id="b60cf-131">OUTPUTS</span></span>

### <span data-ttu-id="b60cf-132">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="b60cf-132">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="b60cf-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b60cf-133">NOTES</span></span>

## <span data-ttu-id="b60cf-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b60cf-134">RELATED LINKS</span></span>
