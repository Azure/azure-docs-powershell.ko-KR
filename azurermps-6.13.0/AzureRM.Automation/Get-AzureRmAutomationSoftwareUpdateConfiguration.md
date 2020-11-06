---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: f4d17fa6cdcb64aab2ab373420891f686facfdf8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534492"
---
# <span data-ttu-id="99840-101">Get-AzureRmAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="99840-101">Get-AzureRmAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="99840-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99840-102">SYNOPSIS</span></span>
<span data-ttu-id="99840-103">Azure 자동화 소프트웨어 업데이트 구성의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="99840-103">Gets a list of azure automation software update configurations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99840-104">구문과</span><span class="sxs-lookup"><span data-stu-id="99840-104">SYNTAX</span></span>

### <span data-ttu-id="99840-105">ByAll (기본값)</span><span class="sxs-lookup"><span data-stu-id="99840-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationSoftwareUpdateConfiguration [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99840-106">ByName</span><span class="sxs-lookup"><span data-stu-id="99840-106">ByName</span></span>
```
Get-AzureRmAutomationSoftwareUpdateConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99840-107">ByVMId</span><span class="sxs-lookup"><span data-stu-id="99840-107">ByVMId</span></span>
```
Get-AzureRmAutomationSoftwareUpdateConfiguration -AzureVMResourceId <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99840-108">설명은</span><span class="sxs-lookup"><span data-stu-id="99840-108">DESCRIPTION</span></span>
<span data-ttu-id="99840-109">Get-AzureRmAutomationSoftwareUpdateConfiguration 소프트웨어 업데이트 구성 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="99840-109">The Get-AzureRmAutomationSoftwareUpdateConfiguration returns a list of software update configurations.</span></span> <span data-ttu-id="99840-110">특정 소프트웨어 업데이트 구성을 가져오려면 name 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99840-110">To get a specific software update configuration, specify the name parameter.</span></span> <span data-ttu-id="99840-111">이 가상 컴퓨터에 대 한 azure 리소스 Id를 지정 하 여 특정 azure 가상 컴퓨터를 대상으로 하는 소프트웨어 업데이트 구성을 나열할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="99840-111">You can also list software update configurations targeting specific azure virtual machine by specifying the azure resource Id for this virtual machine.</span></span>

## <span data-ttu-id="99840-112">예제의</span><span class="sxs-lookup"><span data-stu-id="99840-112">EXAMPLES</span></span>

### <span data-ttu-id="99840-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="99840-113">Example 1</span></span>
<span data-ttu-id="99840-114">이름별로 azure automation 소프트웨어 업데이트 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="99840-114">Get an azure automation software update configuration by name.</span></span>

```powershell
PS C:\> Get-AzureRmAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" -AutomationAccountName "myaccount" -Name "MyWeeklySchedule"

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

## <span data-ttu-id="99840-115">변수</span><span class="sxs-lookup"><span data-stu-id="99840-115">PARAMETERS</span></span>

### <span data-ttu-id="99840-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="99840-116">-AutomationAccountName</span></span>
<span data-ttu-id="99840-117">Automation 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="99840-117">The automation account name.</span></span>

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

### <span data-ttu-id="99840-118">-AzureVMResourceId</span><span class="sxs-lookup"><span data-stu-id="99840-118">-AzureVMResourceId</span></span>
<span data-ttu-id="99840-119">가상 컴퓨터의 Azure 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="99840-119">Azure resource Id of the virtual machine.</span></span>

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

### <span data-ttu-id="99840-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99840-120">-DefaultProfile</span></span>
<span data-ttu-id="99840-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="99840-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99840-122">-이름</span><span class="sxs-lookup"><span data-stu-id="99840-122">-Name</span></span>
<span data-ttu-id="99840-123">소프트웨어 업데이트 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="99840-123">Name of the software update configuration.</span></span>

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

### <span data-ttu-id="99840-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99840-124">-ResourceGroupName</span></span>
<span data-ttu-id="99840-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="99840-125">The resource group name.</span></span>

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

### <span data-ttu-id="99840-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99840-126">CommonParameters</span></span>
<span data-ttu-id="99840-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="99840-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99840-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99840-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99840-129">입력</span><span class="sxs-lookup"><span data-stu-id="99840-129">INPUTS</span></span>

### <span data-ttu-id="99840-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="99840-130">System.String</span></span>

## <span data-ttu-id="99840-131">출력</span><span class="sxs-lookup"><span data-stu-id="99840-131">OUTPUTS</span></span>

### <span data-ttu-id="99840-132">UpdateManagement. SoftwareUpdateConfiguration에 대 한 자동.</span><span class="sxs-lookup"><span data-stu-id="99840-132">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="99840-133">상속자</span><span class="sxs-lookup"><span data-stu-id="99840-133">NOTES</span></span>

## <span data-ttu-id="99840-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="99840-134">RELATED LINKS</span></span>
