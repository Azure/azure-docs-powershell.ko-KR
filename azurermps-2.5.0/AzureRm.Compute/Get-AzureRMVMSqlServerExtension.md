---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CAA3E6A9-7E1A-4D57-A269-0B2D3D9C3BEC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmsqlserverextension
schema: 2.0.0
ms.openlocfilehash: 6b02a83c7664fa460cd4ebd25a1754a8bc57e784
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93883177"
---
# <span data-ttu-id="bfdb4-101">Get-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="bfdb4-101">Get-AzureRmVMSqlServerExtension</span></span>

## <span data-ttu-id="bfdb4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfdb4-102">SYNOPSIS</span></span>
<span data-ttu-id="bfdb4-103">가상 컴퓨터의 SQL Server 확장에 대 한 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bfdb4-103">Gets the settings for a SQL Server extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bfdb4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bfdb4-104">SYNTAX</span></span>

```
Get-AzureRmVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bfdb4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="bfdb4-105">DESCRIPTION</span></span>
<span data-ttu-id="bfdb4-106">**AzureRmVMSqlServerExtension** cmdlet은 가상 컴퓨터의 IAAS (SQL Server 인프라 as Services) 에이전트 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bfdb4-106">The **Get-AzureRmVMSqlServerExtension** cmdlet gets the settings of the SQL Server infrastructure as a service (IaaS) Agent on a virtual machine.</span></span>

## <span data-ttu-id="bfdb4-107">예제의</span><span class="sxs-lookup"><span data-stu-id="bfdb4-107">EXAMPLES</span></span>

### <span data-ttu-id="bfdb4-108">예제 1: 가상 컴퓨터에서 SQL Server 확장의 설정 가져오기</span><span class="sxs-lookup"><span data-stu-id="bfdb4-108">Example 1: Get the settings of a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzureRmVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="bfdb4-109">이 명령은 ContosoVM07 이라는 가상 컴퓨터에서 SQL Server 확장의 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bfdb4-109">This command gets the settings of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

### <span data-ttu-id="bfdb4-110">예제 2: 파이프라인을 사용 하 여 설정 가져오기</span><span class="sxs-lookup"><span data-stu-id="bfdb4-110">Example 2: Get the settings by using the pipeline</span></span>
```
PS C:\> Get-AzureRmVM -ServiceName "Service08" -Name "ContosoVM22" | Get-AzureRmVMSqlServerExtension
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="bfdb4-111">이 명령은 Get-AzureRmVM cmdlet을 사용 하 여 서비스 Service08에서 ContosoVM22 라는 가상 컴퓨터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bfdb4-111">This command gets the virtual machine named ContosoVM22 on the service Service08 by using the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="bfdb4-112">이 명령은 파이프라인 연산자를 사용 하 여 결과를 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfdb4-112">The command passes the results to the current cmdlet by using the pipeline operator.</span></span>

<span data-ttu-id="bfdb4-113">현재 명령은 해당 가상 컴퓨터에서 SQL Server IaaS 에이전트의 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bfdb4-113">The current command gets the settings of the SQL Server IaaS Agent on that virtual machine.</span></span>

### <span data-ttu-id="bfdb4-114">예제 3: 특정 SQL Server 버전의 설정 가져오기</span><span class="sxs-lookup"><span data-stu-id="bfdb4-114">Example 3: Get the settings of specific SQL Server version</span></span>
```
PS C:\> Get-AzureRmVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07" -Version "1.0"
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="bfdb4-115">이 명령은 ContosoVM07 이라는 가상 컴퓨터에서 SQL Server 확장의 버전 1.0에 대 한 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bfdb4-115">This command gets the settings of version 1.0 of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

## <span data-ttu-id="bfdb4-116">변수</span><span class="sxs-lookup"><span data-stu-id="bfdb4-116">PARAMETERS</span></span>

### <span data-ttu-id="bfdb4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfdb4-117">-DefaultProfile</span></span>
<span data-ttu-id="bfdb4-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bfdb4-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfdb4-119">-이름</span><span class="sxs-lookup"><span data-stu-id="bfdb4-119">-Name</span></span>
<span data-ttu-id="bfdb4-120">확장 하는 SQL Server의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfdb4-120">Specifies the name of the SQL Server the extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfdb4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfdb4-121">-ResourceGroupName</span></span>
<span data-ttu-id="bfdb4-122">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfdb4-122">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfdb4-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="bfdb4-123">-VMName</span></span>
<span data-ttu-id="bfdb4-124">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfdb4-124">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfdb4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfdb4-125">CommonParameters</span></span>
<span data-ttu-id="bfdb4-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfdb4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfdb4-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfdb4-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfdb4-128">입력</span><span class="sxs-lookup"><span data-stu-id="bfdb4-128">INPUTS</span></span>

### <span data-ttu-id="bfdb4-129">않아야</span><span class="sxs-lookup"><span data-stu-id="bfdb4-129">None</span></span>
<span data-ttu-id="bfdb4-130">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bfdb4-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bfdb4-131">출력</span><span class="sxs-lookup"><span data-stu-id="bfdb4-131">OUTPUTS</span></span>

### <span data-ttu-id="bfdb4-132">VirtualMachineSqlServerExtensionContext를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfdb4-132">Microsoft.Azure.Commands.Compute.VirtualMachineSqlServerExtensionContext</span></span>

## <span data-ttu-id="bfdb4-133">상속자</span><span class="sxs-lookup"><span data-stu-id="bfdb4-133">NOTES</span></span>

## <span data-ttu-id="bfdb4-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bfdb4-134">RELATED LINKS</span></span>

[<span data-ttu-id="bfdb4-135">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="bfdb4-135">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="bfdb4-136">제거-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="bfdb4-136">Remove-AzureRmVMSqlServerExtension</span></span>](./Remove-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="bfdb4-137">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="bfdb4-137">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


