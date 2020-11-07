---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CAA3E6A9-7E1A-4D57-A269-0B2D3D9C3BEC
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSqlServerExtension.md
ms.openlocfilehash: 9f0f9cfd25e630f0525a724fbec8f8b26ef872db
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701335"
---
# <span data-ttu-id="45af1-101">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="45af1-101">Get-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="45af1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45af1-102">SYNOPSIS</span></span>
<span data-ttu-id="45af1-103">가상 컴퓨터의 SQL Server 확장에 대 한 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="45af1-103">Gets the settings for a SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="45af1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="45af1-104">SYNTAX</span></span>

```
Get-AzVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45af1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="45af1-105">DESCRIPTION</span></span>
<span data-ttu-id="45af1-106">**AzVMSqlServerExtension** cmdlet은 가상 컴퓨터의 IAAS (SQL Server 인프라 as Services) 에이전트 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="45af1-106">The **Get-AzVMSqlServerExtension** cmdlet gets the settings of the SQL Server infrastructure as a service (IaaS) Agent on a virtual machine.</span></span>

## <span data-ttu-id="45af1-107">예제의</span><span class="sxs-lookup"><span data-stu-id="45af1-107">EXAMPLES</span></span>

### <span data-ttu-id="45af1-108">예제 1: 가상 컴퓨터에서 SQL Server 확장의 설정 가져오기</span><span class="sxs-lookup"><span data-stu-id="45af1-108">Example 1: Get the settings of a SQL Server extension on a virtual machine</span></span>
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

<span data-ttu-id="45af1-109">이 명령은 ContosoVM07 이라는 가상 컴퓨터에서 SQL Server 확장의 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="45af1-109">This command gets the settings of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

### <span data-ttu-id="45af1-110">예제 2: 파이프라인을 사용 하 여 설정 가져오기</span><span class="sxs-lookup"><span data-stu-id="45af1-110">Example 2: Get the settings by using the pipeline</span></span>
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

<span data-ttu-id="45af1-111">이 명령은 Get-AzVM cmdlet을 사용 하 여 서비스 Service08에서 ContosoVM22 라는 가상 컴퓨터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="45af1-111">This command gets the virtual machine named ContosoVM22 on the service Service08 by using the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="45af1-112">이 명령은 파이프라인 연산자를 사용 하 여 결과를 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="45af1-112">The command passes the results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="45af1-113">현재 명령은 해당 가상 컴퓨터에서 SQL Server IaaS 에이전트의 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="45af1-113">The current command gets the settings of the SQL Server IaaS Agent on that virtual machine.</span></span>

### <span data-ttu-id="45af1-114">예제 3: 특정 SQL Server 버전의 설정 가져오기</span><span class="sxs-lookup"><span data-stu-id="45af1-114">Example 3: Get the settings of specific SQL Server version</span></span>
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

<span data-ttu-id="45af1-115">이 명령은 ContosoVM07 이라는 가상 컴퓨터에서 SQL Server 확장의 버전 1.0에 대 한 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="45af1-115">This command gets the settings of version 1.0 of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

## <span data-ttu-id="45af1-116">변수</span><span class="sxs-lookup"><span data-stu-id="45af1-116">PARAMETERS</span></span>

### <span data-ttu-id="45af1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45af1-117">-DefaultProfile</span></span>
<span data-ttu-id="45af1-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="45af1-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45af1-119">-이름</span><span class="sxs-lookup"><span data-stu-id="45af1-119">-Name</span></span>
<span data-ttu-id="45af1-120">확장 하는 SQL Server의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="45af1-120">Specifies the name of the SQL Server the extension.</span></span>

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

### <span data-ttu-id="45af1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45af1-121">-ResourceGroupName</span></span>
<span data-ttu-id="45af1-122">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="45af1-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="45af1-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="45af1-123">-VMName</span></span>
<span data-ttu-id="45af1-124">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="45af1-124">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="45af1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45af1-125">CommonParameters</span></span>
<span data-ttu-id="45af1-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="45af1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45af1-127">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="45af1-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45af1-128">입력</span><span class="sxs-lookup"><span data-stu-id="45af1-128">INPUTS</span></span>

### <span data-ttu-id="45af1-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="45af1-129">System.String</span></span>

## <span data-ttu-id="45af1-130">출력</span><span class="sxs-lookup"><span data-stu-id="45af1-130">OUTPUTS</span></span>

### <span data-ttu-id="45af1-131">VirtualMachineSqlServerExtensionContext를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="45af1-131">Microsoft.Azure.Commands.Compute.VirtualMachineSqlServerExtensionContext</span></span>

## <span data-ttu-id="45af1-132">상속자</span><span class="sxs-lookup"><span data-stu-id="45af1-132">NOTES</span></span>

## <span data-ttu-id="45af1-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="45af1-133">RELATED LINKS</span></span>

[<span data-ttu-id="45af1-134">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="45af1-134">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="45af1-135">제거-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="45af1-135">Remove-AzVMSqlServerExtension</span></span>](./Remove-AzVMSqlServerExtension.md)

[<span data-ttu-id="45af1-136">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="45af1-136">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


