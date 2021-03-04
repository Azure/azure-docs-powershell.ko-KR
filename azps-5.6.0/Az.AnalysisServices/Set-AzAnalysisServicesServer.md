---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/powershell/module/az.analysisservices/set-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Set-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Set-AzAnalysisServicesServer.md
ms.openlocfilehash: b39da37f41e3a18bc70f25fe36d67301e49867c9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959307"
---
# <span data-ttu-id="c222b-101">Set-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="c222b-101">Set-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="c222b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c222b-102">SYNOPSIS</span></span>
<span data-ttu-id="c222b-103">Analysis Services 서버 인스턴스 수정</span><span class="sxs-lookup"><span data-stu-id="c222b-103">Modifies  an instance of Analysis Services server</span></span>

## <span data-ttu-id="c222b-104">구문</span><span class="sxs-lookup"><span data-stu-id="c222b-104">SYNTAX</span></span>

### <span data-ttu-id="c222b-105">기본값(기본값)</span><span class="sxs-lookup"><span data-stu-id="c222b-105">Default (Default)</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>] [-PassThru]
 [-ReadonlyReplicaCount <Int32>] [-DefaultConnectionMode <String>]
 [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>] [-GatewayResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c222b-106">DisableBackup</span><span class="sxs-lookup"><span data-stu-id="c222b-106">DisableBackup</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-DisableBackup] [-ReadonlyReplicaCount <Int32>]
 [-DefaultConnectionMode <String>] [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c222b-107">DisassociateGateway</span><span class="sxs-lookup"><span data-stu-id="c222b-107">DisassociateGateway</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-ReadonlyReplicaCount <Int32>]
 [-DefaultConnectionMode <String>] [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>]
 [-DisassociateGateway] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c222b-108">설명</span><span class="sxs-lookup"><span data-stu-id="c222b-108">DESCRIPTION</span></span>
<span data-ttu-id="c222b-109">Set-AzAnalysisServicesServer cmdlet은 Analysis Services 서버의 인스턴스를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="c222b-109">The Set-AzAnalysisServicesServer cmdlet modifies an instance of Analysis Services server</span></span>

## <span data-ttu-id="c222b-110">예제</span><span class="sxs-lookup"><span data-stu-id="c222b-110">EXAMPLES</span></span>

### <span data-ttu-id="c222b-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="c222b-111">Example 1</span></span>
```
PS C:\> Set-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup" -Tag "key1:value1,key2:value2" -Administrator "testuser1@contoso.com"
```

<span data-ttu-id="c222b-112">리소스 그룹 테스트 그룹에서 testserver라는 서버를 수정하여 태그를 key1:value1 및 key2:value2 및 관리자로 설정 testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="c222b-112">Modifies the server named testserver in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="c222b-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c222b-113">PARAMETERS</span></span>

### <span data-ttu-id="c222b-114">-Administrator</span><span class="sxs-lookup"><span data-stu-id="c222b-114">-Administrator</span></span>
<span data-ttu-id="c222b-115">서버에서 관리자로 설정할 사용자 또는 그룹의 콤마로 구분된 목록을 나타내는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="c222b-115">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span>
<span data-ttu-id="c222b-116">사용자 또는 그룹은 UPN 형식(예: 또는 user@contoso.comgroups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="c222b-116">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c222b-117">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="c222b-117">-BackupBlobContainerUri</span></span>
<span data-ttu-id="c222b-118">Analysis Services 서버를 백업하기 위한 Blob 컨테이너 Uri</span><span class="sxs-lookup"><span data-stu-id="c222b-118">The blob container Uri for backup the Analysis Services server</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c222b-119">-DefaultConnectionMode</span><span class="sxs-lookup"><span data-stu-id="c222b-119">-DefaultConnectionMode</span></span>
<span data-ttu-id="c222b-120">Analysis 서비스 서버의 기본 연결 모드</span><span class="sxs-lookup"><span data-stu-id="c222b-120">Default connection mode of an Analysis service server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: All, Readonly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c222b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c222b-121">-DefaultProfile</span></span>
<span data-ttu-id="c222b-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c222b-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c222b-123">-DisableBackup</span><span class="sxs-lookup"><span data-stu-id="c222b-123">-DisableBackup</span></span>
<span data-ttu-id="c222b-124">백업 Blob 컨테이너를 사용하지 않도록 설정하는 스위치입니다.</span><span class="sxs-lookup"><span data-stu-id="c222b-124">The switch to disable backup blob container.</span></span>
<span data-ttu-id="c222b-125">백업 Blob 컨테이너를 다시 사용하도록 설정하려면 백업 Blob 컨테이너 Uri를 -BackupBlobContainerUri로 제공하세요.</span><span class="sxs-lookup"><span data-stu-id="c222b-125">To re-enable the backup blob container, please provide the backup blob container Uri as -BackupBlobContainerUri.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableBackup
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c222b-126">-DisassociateGateway</span><span class="sxs-lookup"><span data-stu-id="c222b-126">-DisassociateGateway</span></span>
<span data-ttu-id="c222b-127">분석 서버에서 게이트웨이 리소스의 연결 해리</span><span class="sxs-lookup"><span data-stu-id="c222b-127">Disassociate Gateway resource from an Analysis server</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisassociateGateway
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c222b-128">-FirewallConfig</span><span class="sxs-lookup"><span data-stu-id="c222b-128">-FirewallConfig</span></span>
<span data-ttu-id="c222b-129">분석 서버의 방화벽 구성</span><span class="sxs-lookup"><span data-stu-id="c222b-129">Firewall config of an Analysis server</span></span>

```yaml
Type: Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c222b-130">-GatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="c222b-130">-GatewayResourceId</span></span>
<span data-ttu-id="c222b-131">Analysis 서버에 연결하기 위한 게이트웨이 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="c222b-131">Gateway resource Id to associate to an Analysis server</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c222b-132">-Name</span><span class="sxs-lookup"><span data-stu-id="c222b-132">-Name</span></span>
<span data-ttu-id="c222b-133">Analysis Services 서버 이름</span><span class="sxs-lookup"><span data-stu-id="c222b-133">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="c222b-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c222b-134">-PassThru</span></span>
<span data-ttu-id="c222b-135">작업이 성공적으로 완료되면 삭제된 서버 세부 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="c222b-135">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="c222b-136">-ReadonlyReplicaCount</span><span class="sxs-lookup"><span data-stu-id="c222b-136">-ReadonlyReplicaCount</span></span>
<span data-ttu-id="c222b-137">Analysis 서비스 서버의 복제본 수만 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="c222b-137">Read only replica count of an Analysis service server</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c222b-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c222b-138">-ResourceGroupName</span></span>
<span data-ttu-id="c222b-139">서버가 속한 Azure 리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="c222b-139">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c222b-140">-Sku</span><span class="sxs-lookup"><span data-stu-id="c222b-140">-Sku</span></span>
<span data-ttu-id="c222b-141">서버의 Sku의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c222b-141">The name of the Sku for the server.</span></span>
<span data-ttu-id="c222b-142">지원되는 값은 표준 계층의 'S0', 'S1', 'S2', 'S4', 'S8', 'S9', 'S8v2', 'S9v2'입니다. 'B1', 기본 계층의 'B2', 개발 계층의 'D1'입니다.</span><span class="sxs-lookup"><span data-stu-id="c222b-142">The supported values are 'S0', 'S1', 'S2', 'S4', 'S8', 'S9', 'S8v2', 'S9v2' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

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

### <span data-ttu-id="c222b-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="c222b-143">-Tag</span></span>
<span data-ttu-id="c222b-144">서버의 태그로 설정된 해시 테이블의 형태로 키 값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="c222b-144">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c222b-145">-확인</span><span class="sxs-lookup"><span data-stu-id="c222b-145">-Confirm</span></span>
<span data-ttu-id="c222b-146">사용자에게 작업을 수행할지 여부를 확인하라는 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="c222b-146">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c222b-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c222b-147">-WhatIf</span></span>
<span data-ttu-id="c222b-148">현재 작업이 실제로 수행하지 않고 수행할 작업을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="c222b-148">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c222b-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c222b-149">CommonParameters</span></span>
<span data-ttu-id="c222b-150">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c222b-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c222b-151">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c222b-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c222b-152">입력</span><span class="sxs-lookup"><span data-stu-id="c222b-152">INPUTS</span></span>

### <span data-ttu-id="c222b-153">System.String</span><span class="sxs-lookup"><span data-stu-id="c222b-153">System.String</span></span>

### <span data-ttu-id="c222b-154">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="c222b-154">System.Collections.Hashtable</span></span>

### <span data-ttu-id="c222b-155">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c222b-155">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="c222b-156">System.Int32</span><span class="sxs-lookup"><span data-stu-id="c222b-156">System.Int32</span></span>

### <span data-ttu-id="c222b-157">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="c222b-157">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="c222b-158">출력</span><span class="sxs-lookup"><span data-stu-id="c222b-158">OUTPUTS</span></span>

### <span data-ttu-id="c222b-159">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="c222b-159">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="c222b-160">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c222b-160">NOTES</span></span>
<span data-ttu-id="c222b-161">별칭: Set-AzAs</span><span class="sxs-lookup"><span data-stu-id="c222b-161">Alias: Set-AzAs</span></span>

## <span data-ttu-id="c222b-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c222b-162">RELATED LINKS</span></span>

[<span data-ttu-id="c222b-163">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="c222b-163">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="c222b-164">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="c222b-164">Remove-AzAnalysisServicesServer</span></span>](./Remove-AzAnalysisServicesServer.md)
