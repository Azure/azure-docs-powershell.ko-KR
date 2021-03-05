---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: 99f2c14cbc3c3f652df062bb3bf806e89ca05f06
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014192"
---
# <span data-ttu-id="9a0d8-101">Get-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="9a0d8-101">Get-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="9a0d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a0d8-102">SYNOPSIS</span></span>
<span data-ttu-id="9a0d8-103">Azure Automation 소프트웨어 업데이트 구성의 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9a0d8-103">Gets a list of azure automation software update configurations.</span></span>

## <span data-ttu-id="9a0d8-104">구문</span><span class="sxs-lookup"><span data-stu-id="9a0d8-104">SYNTAX</span></span>

### <span data-ttu-id="9a0d8-105">ByAll(기본값)</span><span class="sxs-lookup"><span data-stu-id="9a0d8-105">ByAll (Default)</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a0d8-106">ByName</span><span class="sxs-lookup"><span data-stu-id="9a0d8-106">ByName</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a0d8-107">ByVMId</span><span class="sxs-lookup"><span data-stu-id="9a0d8-107">ByVMId</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration -AzureVMResourceId <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a0d8-108">설명</span><span class="sxs-lookup"><span data-stu-id="9a0d8-108">DESCRIPTION</span></span>
<span data-ttu-id="9a0d8-109">이 Get-AzAutomationSoftwareUpdateConfiguration 업데이트 구성 목록을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="9a0d8-109">The Get-AzAutomationSoftwareUpdateConfiguration returns a list of software update configurations.</span></span> <span data-ttu-id="9a0d8-110">특정 소프트웨어 업데이트 구성을 얻하려면 이름 매개 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9a0d8-110">To get a specific software update configuration, specify the name parameter.</span></span> <span data-ttu-id="9a0d8-111">또한 이 가상 머신에 대한 Azure 리소스 ID를 지정하여 특정 Azure 가상 머신을 대상으로 하는 소프트웨어 업데이트 구성을 나열할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9a0d8-111">You can also list software update configurations targeting specific azure virtual machine by specifying the azure resource Id for this virtual machine.</span></span>

## <span data-ttu-id="9a0d8-112">예제</span><span class="sxs-lookup"><span data-stu-id="9a0d8-112">EXAMPLES</span></span>

### <span data-ttu-id="9a0d8-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="9a0d8-113">Example 1</span></span>
<span data-ttu-id="9a0d8-114">이름으로 Azure Automation 소프트웨어 업데이트 구성을 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="9a0d8-114">Get an azure automation software update configuration by name.</span></span>

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

## <span data-ttu-id="9a0d8-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="9a0d8-115">PARAMETERS</span></span>

### <span data-ttu-id="9a0d8-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9a0d8-116">-AutomationAccountName</span></span>
<span data-ttu-id="9a0d8-117">자동화 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9a0d8-117">The automation account name.</span></span>

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

### <span data-ttu-id="9a0d8-118">-AzureVMResourceId</span><span class="sxs-lookup"><span data-stu-id="9a0d8-118">-AzureVMResourceId</span></span>
<span data-ttu-id="9a0d8-119">가상 머신의 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="9a0d8-119">Azure resource Id of the virtual machine.</span></span>

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

### <span data-ttu-id="9a0d8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a0d8-120">-DefaultProfile</span></span>
<span data-ttu-id="9a0d8-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9a0d8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a0d8-122">-Name</span><span class="sxs-lookup"><span data-stu-id="9a0d8-122">-Name</span></span>
<span data-ttu-id="9a0d8-123">소프트웨어 업데이트 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9a0d8-123">Name of the software update configuration.</span></span>

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

### <span data-ttu-id="9a0d8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a0d8-124">-ResourceGroupName</span></span>
<span data-ttu-id="9a0d8-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9a0d8-125">The resource group name.</span></span>

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

### <span data-ttu-id="9a0d8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a0d8-126">CommonParameters</span></span>
<span data-ttu-id="9a0d8-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9a0d8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a0d8-128">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9a0d8-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a0d8-129">입력</span><span class="sxs-lookup"><span data-stu-id="9a0d8-129">INPUTS</span></span>

### <span data-ttu-id="9a0d8-130">System.String</span><span class="sxs-lookup"><span data-stu-id="9a0d8-130">System.String</span></span>

## <span data-ttu-id="9a0d8-131">출력</span><span class="sxs-lookup"><span data-stu-id="9a0d8-131">OUTPUTS</span></span>

### <span data-ttu-id="9a0d8-132">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="9a0d8-132">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="9a0d8-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9a0d8-133">NOTES</span></span>

## <span data-ttu-id="9a0d8-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9a0d8-134">RELATED LINKS</span></span>
