---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3B15C734-DF57-433A-8854-ACE2B35FF6CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAEMExtension.md
ms.openlocfilehash: b476254d5b9236aa95a30832499aca65a8a110c0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356277"
---
# <span data-ttu-id="ba04b-101">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="ba04b-101">Set-AzVMAEMExtension</span></span>

## <span data-ttu-id="ba04b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba04b-102">SYNOPSIS</span></span>
<span data-ttu-id="ba04b-103">SAP 시스템에 대한 모니터링을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ba04b-103">Enables support for monitoring for SAP systems.</span></span>

## <span data-ttu-id="ba04b-104">구문</span><span class="sxs-lookup"><span data-stu-id="ba04b-104">SYNTAX</span></span>

```
Set-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [-EnableWAD]
 [[-WADStorageAccountName] <String>] [[-OSType] <String>] [-SkipStorage] [-NoWait]
 [-SetAccessToIndividualResources] [-InstallNewExtension] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ba04b-105">설명</span><span class="sxs-lookup"><span data-stu-id="ba04b-105">DESCRIPTION</span></span>
<span data-ttu-id="ba04b-106">**Set-AzVMAEMExtension** cmdlet은 가상 머신에 설치된 SAP 시스템에 대한 모니터링 지원을 사용하도록 설정하거나 업데이트하도록 가상 머신의 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ba04b-106">The **Set-AzVMAEMExtension** cmdlet updates the configuration of a virtual machine to enable or update the support for monitoring for SAP systems that are installed on the virtual machine.</span></span>
<span data-ttu-id="ba04b-107">이 cmdlet은 성능 데이터를 수집하고 SAP 시스템에 대해 검색할 수 있는 AEM(Azure 고급 모니터링) 확장을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="ba04b-107">The cmdlet installs the Azure Enhanced Monitoring (AEM) extension that collects the performance data and makes it discoverable for the SAP system.</span></span>

## <span data-ttu-id="ba04b-108">예제</span><span class="sxs-lookup"><span data-stu-id="ba04b-108">EXAMPLES</span></span>

### <span data-ttu-id="ba04b-109">예제 1: AEM 확장 사용</span><span class="sxs-lookup"><span data-stu-id="ba04b-109">Example 1: Use AEM extension</span></span>
```
PS C:\> Set-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server" -WADStorageAccountName "stdstorage"
```

<span data-ttu-id="ba04b-110">이 명령은 AEM 확장을 사용하도록 contoso-server라는 가상 머신을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="ba04b-110">This command configures the virtual machine named contoso-server to use the AEM extension.</span></span>
<span data-ttu-id="ba04b-111">이 명령은 stdstorage라는 저장소 계정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ba04b-111">The command specifies the storage account named stdstorage.</span></span>

## <span data-ttu-id="ba04b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba04b-112">PARAMETERS</span></span>

### <span data-ttu-id="ba04b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba04b-113">-DefaultProfile</span></span>
<span data-ttu-id="ba04b-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ba04b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba04b-115">-EnableWAD</span><span class="sxs-lookup"><span data-stu-id="ba04b-115">-EnableWAD</span></span>
<span data-ttu-id="ba04b-116">이 매개 변수가 제공된 경우 commandlet은 이 가상 머신에 Windows Azure 진단을 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="ba04b-116">If this parameter is provided, the commandlet will enable Windows Azure Diagnostics for this virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba04b-117">-InstallNewExtension</span><span class="sxs-lookup"><span data-stu-id="ba04b-117">-InstallNewExtension</span></span>
<span data-ttu-id="ba04b-118">SAP용 새 VM 확장을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="ba04b-118">Install the new VM Extension for SAP.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba04b-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ba04b-119">-NoWait</span></span>
<span data-ttu-id="ba04b-120">작업을 시작하고 작업이 완료되기 전에 즉시 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ba04b-120">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="ba04b-121">작업이 성공적으로 완료됐는지 확인하기 위해 다른 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba04b-121">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="ba04b-122">-OSType</span><span class="sxs-lookup"><span data-stu-id="ba04b-122">-OSType</span></span>
<span data-ttu-id="ba04b-123">운영 체제 디스크의 운영 체제 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ba04b-123">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="ba04b-124">운영 체제 디스크에 형식이 없는 경우 이 매개 변수를 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba04b-124">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="ba04b-125">이 매개 변수에 허용되는 값은 Windows 및 Linux입니다.</span><span class="sxs-lookup"><span data-stu-id="ba04b-125">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba04b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba04b-126">-ResourceGroupName</span></span>
<span data-ttu-id="ba04b-127">이 cmdlet이 수정하는 가상 머신의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ba04b-127">Specifies the name of the resource group of the virtual machine that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="ba04b-128">-SetAccessToIndividualResources</span><span class="sxs-lookup"><span data-stu-id="ba04b-128">-SetAccessToIndividualResources</span></span>
<span data-ttu-id="ba04b-129">VM ID의 액세스를 개별 리소스(예: 전체 리소스 그룹 대신 데이터 디스크)로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="ba04b-129">Sets the access of the VM identity to the individual resources, e.g. data disks instead of the complete resource group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba04b-130">-SkipStorage</span><span class="sxs-lookup"><span data-stu-id="ba04b-130">-SkipStorage</span></span>
<span data-ttu-id="ba04b-131">이 cmdlet이 저장소 구성을 건너뛰고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba04b-131">Indicates that this cmdlet skips configuration of storage.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba04b-132">-VMName</span><span class="sxs-lookup"><span data-stu-id="ba04b-132">-VMName</span></span>
<span data-ttu-id="ba04b-133">가상 머신의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ba04b-133">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="ba04b-134">이 cmdlet은 이 매개 변수가 지정하는 가상 머신에 대한 AEM 확장을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="ba04b-134">This cmdlet adds the AEM extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba04b-135">-WADStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ba04b-135">-WADStorageAccountName</span></span>
<span data-ttu-id="ba04b-136">이 cmdlet이 LinuxDiagnostics 또는 IaaSDiagnostics 확장을 구성하는 데 사용하는 저장소 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ba04b-136">Specifies the name of the storage account that this cmdlet uses to configure the LinuxDiagnostics or IaaSDiagnostics extension.</span></span>
<span data-ttu-id="ba04b-137">가상 머신에서 표준 저장소 계정을 사용하지 않는 경우 이 매개 변수에 대한 값을 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba04b-137">If the virtual machine does not use a standard storage account, you must specify a value for this parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba04b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba04b-138">CommonParameters</span></span>
<span data-ttu-id="ba04b-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ba04b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba04b-140">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ba04b-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba04b-141">입력</span><span class="sxs-lookup"><span data-stu-id="ba04b-141">INPUTS</span></span>

### <span data-ttu-id="ba04b-142">System.String</span><span class="sxs-lookup"><span data-stu-id="ba04b-142">System.String</span></span>

## <span data-ttu-id="ba04b-143">출력</span><span class="sxs-lookup"><span data-stu-id="ba04b-143">OUTPUTS</span></span>

### <span data-ttu-id="ba04b-144">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="ba04b-144">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="ba04b-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ba04b-145">NOTES</span></span>

## <span data-ttu-id="ba04b-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ba04b-146">RELATED LINKS</span></span>

[<span data-ttu-id="ba04b-147">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="ba04b-147">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="ba04b-148">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="ba04b-148">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="ba04b-149">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="ba04b-149">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)


