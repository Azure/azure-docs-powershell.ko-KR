---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3B15C734-DF57-433A-8854-ACE2B35FF6CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAEMExtension.md
ms.openlocfilehash: d79be4ce619d8673a8b3811eb5fa2e0c3602beb8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868898"
---
# <span data-ttu-id="5dae7-101">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="5dae7-101">Set-AzVMAEMExtension</span></span>

## <span data-ttu-id="5dae7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5dae7-102">SYNOPSIS</span></span>
<span data-ttu-id="5dae7-103">SAP 시스템에 대 한 모니터링 지원을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dae7-103">Enables support for monitoring for SAP systems.</span></span>

## <span data-ttu-id="5dae7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5dae7-104">SYNTAX</span></span>

```
Set-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [-EnableWAD]
 [[-WADStorageAccountName] <String>] [[-OSType] <String>] [-SkipStorage]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5dae7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5dae7-105">DESCRIPTION</span></span>
<span data-ttu-id="5dae7-106">**AzVMAEMExtension** cmdlet은 가상 컴퓨터에 설치 된 SAP 시스템에 대 한 모니터링 지원을 사용 하거나 업데이트 하도록 가상 컴퓨터의 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dae7-106">The **Set-AzVMAEMExtension** cmdlet updates the configuration of a virtual machine to enable or update the support for monitoring for SAP systems that are installed on the virtual machine.</span></span>
<span data-ttu-id="5dae7-107">Cmdlet은 성능 데이터를 수집 하 고 SAP 시스템을 검색할 수 있도록 하는 AEM (Azure 확장 모니터링) 확장을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dae7-107">The cmdlet installs the Azure Enhanced Monitoring (AEM) extension that collects the performance data and makes it discoverable for the SAP system.</span></span>

## <span data-ttu-id="5dae7-108">예제의</span><span class="sxs-lookup"><span data-stu-id="5dae7-108">EXAMPLES</span></span>

### <span data-ttu-id="5dae7-109">예제 1: AEM extension 사용</span><span class="sxs-lookup"><span data-stu-id="5dae7-109">Example 1: Use AEM extension</span></span>
```
PS C:\> Set-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server" -WADStorageAccountName "stdstorage"
```

<span data-ttu-id="5dae7-110">이 명령은 AEM 확장명을 사용 하도록 contoso-server 라는 가상 컴퓨터를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dae7-110">This command configures the virtual machine named contoso-server to use the AEM extension.</span></span>
<span data-ttu-id="5dae7-111">이 명령은 stdstorage 라는 저장소 계정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dae7-111">The command specifies the storage account named stdstorage.</span></span>

## <span data-ttu-id="5dae7-112">변수</span><span class="sxs-lookup"><span data-stu-id="5dae7-112">PARAMETERS</span></span>

### <span data-ttu-id="5dae7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dae7-113">-DefaultProfile</span></span>
<span data-ttu-id="5dae7-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5dae7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5dae7-115">-EnableWAD</span><span class="sxs-lookup"><span data-stu-id="5dae7-115">-EnableWAD</span></span>
<span data-ttu-id="5dae7-116">이 매개 변수를 제공 하면이 가상 컴퓨터에 대해 Windows Azure 진단을 사용 하도록 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5dae7-116">If this parameter is provided, the commandlet will enable Windows Azure Diagnostics for this virtual machine.</span></span>

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

### <span data-ttu-id="5dae7-117">-OSType</span><span class="sxs-lookup"><span data-stu-id="5dae7-117">-OSType</span></span>
<span data-ttu-id="5dae7-118">운영 체제 디스크의 운영 체제 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dae7-118">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="5dae7-119">운영 체제 디스크에 형식이 없는 경우이 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dae7-119">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="5dae7-120">이 매개 변수에 허용 되는 값은 Windows 및 Linux입니다.</span><span class="sxs-lookup"><span data-stu-id="5dae7-120">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="5dae7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5dae7-121">-ResourceGroupName</span></span>
<span data-ttu-id="5dae7-122">이 cmdlet이 수정 하는 가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dae7-122">Specifies the name of the resource group of the virtual machine that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="5dae7-123">-SkipStorage</span><span class="sxs-lookup"><span data-stu-id="5dae7-123">-SkipStorage</span></span>
<span data-ttu-id="5dae7-124">이 cmdlet이 저장소 구성을 생략 했음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="5dae7-124">Indicates that this cmdlet skips configuration of storage.</span></span>

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

### <span data-ttu-id="5dae7-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="5dae7-125">-VMName</span></span>
<span data-ttu-id="5dae7-126">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dae7-126">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="5dae7-127">이 cmdlet은이 매개 변수에서 지정 하는 가상 컴퓨터에 대 한 AEM 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dae7-127">This cmdlet adds the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="5dae7-128">-WADStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5dae7-128">-WADStorageAccountName</span></span>
<span data-ttu-id="5dae7-129">이 cmdlet이 LinuxDiagnostics 또는 IaaSDiagnostics 확장을 구성 하는 데 사용 하는 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dae7-129">Specifies the name of the storage account that this cmdlet uses to configure the LinuxDiagnostics or IaaSDiagnostics extension.</span></span>
<span data-ttu-id="5dae7-130">가상 컴퓨터가 표준 저장소 계정을 사용 하지 않는 경우이 매개 변수에 대 한 값을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dae7-130">If the virtual machine does not use a standard storage account, you must specify a value for this parameter.</span></span>

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

### <span data-ttu-id="5dae7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dae7-131">CommonParameters</span></span>
<span data-ttu-id="5dae7-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dae7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dae7-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5dae7-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dae7-134">입력</span><span class="sxs-lookup"><span data-stu-id="5dae7-134">INPUTS</span></span>

### <span data-ttu-id="5dae7-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5dae7-135">System.String</span></span>

## <span data-ttu-id="5dae7-136">출력</span><span class="sxs-lookup"><span data-stu-id="5dae7-136">OUTPUTS</span></span>

### <span data-ttu-id="5dae7-137">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="5dae7-137">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="5dae7-138">상속자</span><span class="sxs-lookup"><span data-stu-id="5dae7-138">NOTES</span></span>

## <span data-ttu-id="5dae7-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5dae7-139">RELATED LINKS</span></span>

[<span data-ttu-id="5dae7-140">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="5dae7-140">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="5dae7-141">제거-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="5dae7-141">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="5dae7-142">테스트-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="5dae7-142">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)


