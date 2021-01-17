---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CAA3E6A9-7E1A-4D57-A269-0B2D3D9C3BEC
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSqlServerExtension.md
ms.openlocfilehash: 7903e13abf7e924898910ad007eefcf6800dcc61
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323063"
---
# <span data-ttu-id="603b0-101">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="603b0-101">Get-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="603b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="603b0-102">SYNOPSIS</span></span>
<span data-ttu-id="603b0-103">가상 머신에서 SQL Server 확장에 대한 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="603b0-103">Gets the settings for a SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="603b0-104">구문</span><span class="sxs-lookup"><span data-stu-id="603b0-104">SYNTAX</span></span>

```
Get-AzVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="603b0-105">설명</span><span class="sxs-lookup"><span data-stu-id="603b0-105">DESCRIPTION</span></span>
<span data-ttu-id="603b0-106">**Get-AzVMSqlServerExtension** cmdlet은 가상 머신에서 SQL Server IaaS(Infrastructure as a Service) 에이전트의 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="603b0-106">The **Get-AzVMSqlServerExtension** cmdlet gets the settings of the SQL Server infrastructure as a service (IaaS) Agent on a virtual machine.</span></span>

## <span data-ttu-id="603b0-107">예제</span><span class="sxs-lookup"><span data-stu-id="603b0-107">EXAMPLES</span></span>

### <span data-ttu-id="603b0-108">예제 1: 가상 머신에서 SQL Server 확장의 설정을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="603b0-108">Example 1: Get the settings of a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="603b0-109">이 명령은 ContosoVM07이라는 가상 SQL Server 확장의 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="603b0-109">This command gets the settings of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

### <span data-ttu-id="603b0-110">예제 2: 파이프라인을 사용하여 설정 얻기</span><span class="sxs-lookup"><span data-stu-id="603b0-110">Example 2: Get the settings by using the pipeline</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service08" -Name "ContosoVM22" | Get-AzVMSqlServerExtension
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="603b0-111">이 명령은 Get-AzVM cmdlet을 사용하여 Service08에서 ContosoVM22라는 가상 머신을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="603b0-111">This command gets the virtual machine named ContosoVM22 on the service Service08 by using the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="603b0-112">이 명령은 파이프라인 연산자를 사용하여 결과를 현재 cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="603b0-112">The command passes the results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="603b0-113">현재 명령은 가상 머신에서 SQL Server IaaS 에이전트의 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="603b0-113">The current command gets the settings of the SQL Server IaaS Agent on that virtual machine.</span></span>

### <span data-ttu-id="603b0-114">예제 3: 특정 버전에 대한 SQL Server</span><span class="sxs-lookup"><span data-stu-id="603b0-114">Example 3: Get the settings of specific SQL Server version</span></span>
```
PS C:\> Get-AzVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07" -Version "1.0"
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="603b0-115">이 명령은 ContosoVM07이라는 가상 머신에서 SQL Server 버전 1.0의 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="603b0-115">This command gets the settings of version 1.0 of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

## <span data-ttu-id="603b0-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="603b0-116">PARAMETERS</span></span>

### <span data-ttu-id="603b0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="603b0-117">-DefaultProfile</span></span>
<span data-ttu-id="603b0-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="603b0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="603b0-119">-Name</span><span class="sxs-lookup"><span data-stu-id="603b0-119">-Name</span></span>
<span data-ttu-id="603b0-120">확장에 대한 SQL Server 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="603b0-120">Specifies the name of the SQL Server the extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="603b0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="603b0-121">-ResourceGroupName</span></span>
<span data-ttu-id="603b0-122">가상 머신의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="603b0-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="603b0-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="603b0-123">-VMName</span></span>
<span data-ttu-id="603b0-124">가상 머신의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="603b0-124">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="603b0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="603b0-125">CommonParameters</span></span>
<span data-ttu-id="603b0-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="603b0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="603b0-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="603b0-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="603b0-128">입력</span><span class="sxs-lookup"><span data-stu-id="603b0-128">INPUTS</span></span>

### <span data-ttu-id="603b0-129">System.String</span><span class="sxs-lookup"><span data-stu-id="603b0-129">System.String</span></span>

## <span data-ttu-id="603b0-130">출력</span><span class="sxs-lookup"><span data-stu-id="603b0-130">OUTPUTS</span></span>

### <span data-ttu-id="603b0-131">Microsoft.Azure.Commands.Compute.VirtualMachineSqlServerExtensionContext</span><span class="sxs-lookup"><span data-stu-id="603b0-131">Microsoft.Azure.Commands.Compute.VirtualMachineSqlServerExtensionContext</span></span>

## <span data-ttu-id="603b0-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="603b0-132">NOTES</span></span>

## <span data-ttu-id="603b0-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="603b0-133">RELATED LINKS</span></span>

[<span data-ttu-id="603b0-134">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="603b0-134">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="603b0-135">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="603b0-135">Remove-AzVMSqlServerExtension</span></span>](./Remove-AzVMSqlServerExtension.md)

[<span data-ttu-id="603b0-136">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="603b0-136">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


