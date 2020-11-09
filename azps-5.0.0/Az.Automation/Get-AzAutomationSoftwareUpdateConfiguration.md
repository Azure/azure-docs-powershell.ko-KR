---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: af11442edfc5acb2d7e9683bc71d7d2e2c87bd5f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94311606"
---
# <span data-ttu-id="8a33e-101">Get-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="8a33e-101">Get-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="8a33e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a33e-102">SYNOPSIS</span></span>
<span data-ttu-id="8a33e-103">Azure 자동화 소프트웨어 업데이트 구성의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8a33e-103">Gets a list of azure automation software update configurations.</span></span>

## <span data-ttu-id="8a33e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8a33e-104">SYNTAX</span></span>

### <span data-ttu-id="8a33e-105">ByAll (기본값)</span><span class="sxs-lookup"><span data-stu-id="8a33e-105">ByAll (Default)</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a33e-106">ByName</span><span class="sxs-lookup"><span data-stu-id="8a33e-106">ByName</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a33e-107">ByVMId</span><span class="sxs-lookup"><span data-stu-id="8a33e-107">ByVMId</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration -AzureVMResourceId <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a33e-108">설명은</span><span class="sxs-lookup"><span data-stu-id="8a33e-108">DESCRIPTION</span></span>
<span data-ttu-id="8a33e-109">Get-AzAutomationSoftwareUpdateConfiguration 소프트웨어 업데이트 구성 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a33e-109">The Get-AzAutomationSoftwareUpdateConfiguration returns a list of software update configurations.</span></span> <span data-ttu-id="8a33e-110">특정 소프트웨어 업데이트 구성을 가져오려면 name 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a33e-110">To get a specific software update configuration, specify the name parameter.</span></span> <span data-ttu-id="8a33e-111">이 가상 컴퓨터에 대 한 azure 리소스 Id를 지정 하 여 특정 azure 가상 컴퓨터를 대상으로 하는 소프트웨어 업데이트 구성을 나열할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8a33e-111">You can also list software update configurations targeting specific azure virtual machine by specifying the azure resource Id for this virtual machine.</span></span>

## <span data-ttu-id="8a33e-112">예제의</span><span class="sxs-lookup"><span data-stu-id="8a33e-112">EXAMPLES</span></span>

### <span data-ttu-id="8a33e-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="8a33e-113">Example 1</span></span>
<span data-ttu-id="8a33e-114">이름별로 azure automation 소프트웨어 업데이트 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8a33e-114">Get an azure automation software update configuration by name.</span></span>

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

## <span data-ttu-id="8a33e-115">변수</span><span class="sxs-lookup"><span data-stu-id="8a33e-115">PARAMETERS</span></span>

### <span data-ttu-id="8a33e-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8a33e-116">-AutomationAccountName</span></span>
<span data-ttu-id="8a33e-117">Automation 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8a33e-117">The automation account name.</span></span>

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

### <span data-ttu-id="8a33e-118">-AzureVMResourceId</span><span class="sxs-lookup"><span data-stu-id="8a33e-118">-AzureVMResourceId</span></span>
<span data-ttu-id="8a33e-119">가상 컴퓨터의 Azure 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="8a33e-119">Azure resource Id of the virtual machine.</span></span>

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

### <span data-ttu-id="8a33e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a33e-120">-DefaultProfile</span></span>
<span data-ttu-id="8a33e-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8a33e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a33e-122">-이름</span><span class="sxs-lookup"><span data-stu-id="8a33e-122">-Name</span></span>
<span data-ttu-id="8a33e-123">소프트웨어 업데이트 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8a33e-123">Name of the software update configuration.</span></span>

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

### <span data-ttu-id="8a33e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a33e-124">-ResourceGroupName</span></span>
<span data-ttu-id="8a33e-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8a33e-125">The resource group name.</span></span>

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

### <span data-ttu-id="8a33e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a33e-126">CommonParameters</span></span>
<span data-ttu-id="8a33e-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a33e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a33e-128">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a33e-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a33e-129">입력</span><span class="sxs-lookup"><span data-stu-id="8a33e-129">INPUTS</span></span>

### <span data-ttu-id="8a33e-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8a33e-130">System.String</span></span>

## <span data-ttu-id="8a33e-131">출력</span><span class="sxs-lookup"><span data-stu-id="8a33e-131">OUTPUTS</span></span>

### <span data-ttu-id="8a33e-132">UpdateManagement. SoftwareUpdateConfiguration에 대 한 자동.</span><span class="sxs-lookup"><span data-stu-id="8a33e-132">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="8a33e-133">상속자</span><span class="sxs-lookup"><span data-stu-id="8a33e-133">NOTES</span></span>

## <span data-ttu-id="8a33e-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8a33e-134">RELATED LINKS</span></span>
