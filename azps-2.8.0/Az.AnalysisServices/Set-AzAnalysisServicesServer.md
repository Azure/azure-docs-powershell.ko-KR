---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/set-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Set-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Set-AzAnalysisServicesServer.md
ms.openlocfilehash: 376dc1cf74f93016cd0ce8e50d298cd2d12d6317
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698153"
---
# <span data-ttu-id="58209-101">Set-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="58209-101">Set-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="58209-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58209-102">SYNOPSIS</span></span>
<span data-ttu-id="58209-103">Analysis Services 서버 인스턴스 수정</span><span class="sxs-lookup"><span data-stu-id="58209-103">Modifies  an instance of Analysis Services server</span></span>

## <span data-ttu-id="58209-104">구문과</span><span class="sxs-lookup"><span data-stu-id="58209-104">SYNTAX</span></span>

### <span data-ttu-id="58209-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="58209-105">Default (Default)</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>] [-PassThru]
 [-ReadonlyReplicaCount <Int32>] [-DefaultConnectionMode <String>]
 [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>] [-GatewayResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58209-106">DisableBackup</span><span class="sxs-lookup"><span data-stu-id="58209-106">DisableBackup</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-DisableBackup] [-ReadonlyReplicaCount <Int32>]
 [-DefaultConnectionMode <String>] [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58209-107">DisassociateGateway</span><span class="sxs-lookup"><span data-stu-id="58209-107">DisassociateGateway</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-ReadonlyReplicaCount <Int32>]
 [-DefaultConnectionMode <String>] [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>]
 [-DisassociateGateway] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58209-108">설명은</span><span class="sxs-lookup"><span data-stu-id="58209-108">DESCRIPTION</span></span>
<span data-ttu-id="58209-109">Set-AzAnalysisServicesServer cmdlet은 Analysis Services 서버의 인스턴스를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58209-109">The Set-AzAnalysisServicesServer cmdlet modifies an instance of Analysis Services server</span></span>

## <span data-ttu-id="58209-110">예제의</span><span class="sxs-lookup"><span data-stu-id="58209-110">EXAMPLES</span></span>

### <span data-ttu-id="58209-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="58209-111">Example 1</span></span>
```
PS C:\> Set-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup" -Tag "key1:value1,key2:value2" -Administrator "testuser1@contoso.com"
```

<span data-ttu-id="58209-112">Resourcegroup에 대 한 testserver 라는 서버를 수정 하 여 태그를 key1로 설정 합니다. value1 및 key2: value2 및 관리자가 testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="58209-112">Modifies the server named testserver in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="58209-113">변수</span><span class="sxs-lookup"><span data-stu-id="58209-113">PARAMETERS</span></span>

### <span data-ttu-id="58209-114">-관리자</span><span class="sxs-lookup"><span data-stu-id="58209-114">-Administrator</span></span>
<span data-ttu-id="58209-115">서버의 관리자로 설정할 사용자 또는 그룹의 쉼표로 구분 된 목록을 나타내는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="58209-115">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span>
<span data-ttu-id="58209-116">사용자 또는 그룹에 UPN 형식 (예: 또는)을 지정 해야 합니다. user@contoso.comgroups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="58209-116">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

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

### <span data-ttu-id="58209-117">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="58209-117">-BackupBlobContainerUri</span></span>
<span data-ttu-id="58209-118">Analysis Services 서버 백업용 blob 컨테이너 Uri</span><span class="sxs-lookup"><span data-stu-id="58209-118">The blob container Uri for backup the Analysis Services server</span></span>

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

### <span data-ttu-id="58209-119">-DefaultConnectionMode</span><span class="sxs-lookup"><span data-stu-id="58209-119">-DefaultConnectionMode</span></span>
<span data-ttu-id="58209-120">Analysis service 서버의 기본 연결 모드</span><span class="sxs-lookup"><span data-stu-id="58209-120">Default connection mode of an Analysis service server</span></span>

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

### <span data-ttu-id="58209-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58209-121">-DefaultProfile</span></span>
<span data-ttu-id="58209-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="58209-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58209-123">-DisableBackup</span><span class="sxs-lookup"><span data-stu-id="58209-123">-DisableBackup</span></span>
<span data-ttu-id="58209-124">백업 blob 컨테이너를 사용 하지 않도록 전환 합니다.</span><span class="sxs-lookup"><span data-stu-id="58209-124">The switch to disable backup blob container.</span></span>
<span data-ttu-id="58209-125">백업 blob 컨테이너를 다시 사용 하도록 설정 하려면 백업 blob 컨테이너 Uri를-BackupBlobContainerUri로 제공 하세요.</span><span class="sxs-lookup"><span data-stu-id="58209-125">To re-enable the backup blob container, please provide the backup blob container Uri as -BackupBlobContainerUri.</span></span>

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

### <span data-ttu-id="58209-126">-DisassociateGateway</span><span class="sxs-lookup"><span data-stu-id="58209-126">-DisassociateGateway</span></span>
<span data-ttu-id="58209-127">분석 서버에서 게이트웨이 리소스의 연관 해제</span><span class="sxs-lookup"><span data-stu-id="58209-127">Disassociate Gateway resource from an Analysis server</span></span>

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

### <span data-ttu-id="58209-128">-FirewallConfig</span><span class="sxs-lookup"><span data-stu-id="58209-128">-FirewallConfig</span></span>
<span data-ttu-id="58209-129">분석 서버의 방화벽 구성</span><span class="sxs-lookup"><span data-stu-id="58209-129">Firewall config of an Analysis server</span></span>

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

### <span data-ttu-id="58209-130">-게이트웨이 Resourceid</span><span class="sxs-lookup"><span data-stu-id="58209-130">-GatewayResourceId</span></span>
<span data-ttu-id="58209-131">분석 서버에 연결 하는 게이트웨이 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="58209-131">Gateway resource Id to associate to an Analysis server</span></span>

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

### <span data-ttu-id="58209-132">-이름</span><span class="sxs-lookup"><span data-stu-id="58209-132">-Name</span></span>
<span data-ttu-id="58209-133">Analysis Services 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="58209-133">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="58209-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="58209-134">-PassThru</span></span>
<span data-ttu-id="58209-135">작업이 성공적으로 완료 되 면 삭제 된 서버 세부 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="58209-135">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="58209-136">-ReadonlyReplicaCount</span><span class="sxs-lookup"><span data-stu-id="58209-136">-ReadonlyReplicaCount</span></span>
<span data-ttu-id="58209-137">분석 서비스 서버의 복제 횟수 읽기</span><span class="sxs-lookup"><span data-stu-id="58209-137">Read only replica count of an Analysis service server</span></span>

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

### <span data-ttu-id="58209-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58209-138">-ResourceGroupName</span></span>
<span data-ttu-id="58209-139">서버가 속한 Azure 리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="58209-139">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="58209-140">-Sku</span><span class="sxs-lookup"><span data-stu-id="58209-140">-Sku</span></span>
<span data-ttu-id="58209-141">서버의 Sku 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="58209-141">The name of the Sku for the server.</span></span>
<span data-ttu-id="58209-142">지원 되는 값은 표준 계층에 대 한 0 ', ' 1 ', ' 2 ', 4 '입니다. 기본 계층에 대 한 ' B1 ', ' B2 ', 개발 계층의 경우 1 '입니다.</span><span class="sxs-lookup"><span data-stu-id="58209-142">The supported values are 'S0', 'S1', 'S2', 'S4' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

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

### <span data-ttu-id="58209-143">태그</span><span class="sxs-lookup"><span data-stu-id="58209-143">-Tag</span></span>
<span data-ttu-id="58209-144">서버에서 태그로 설정 된 해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="58209-144">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

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

### <span data-ttu-id="58209-145">-확인</span><span class="sxs-lookup"><span data-stu-id="58209-145">-Confirm</span></span>
<span data-ttu-id="58209-146">사용자에 게 작업 수행 여부 확인 메시지 표시</span><span class="sxs-lookup"><span data-stu-id="58209-146">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="58209-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58209-147">-WhatIf</span></span>
<span data-ttu-id="58209-148">현재 작업이 실제로 수행 하지 않고 수행 하는 작업에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="58209-148">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="58209-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58209-149">CommonParameters</span></span>
<span data-ttu-id="58209-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="58209-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58209-151">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58209-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58209-152">입력</span><span class="sxs-lookup"><span data-stu-id="58209-152">INPUTS</span></span>

### <span data-ttu-id="58209-153">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="58209-153">System.String</span></span>

### <span data-ttu-id="58209-154">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="58209-154">System.Collections.Hashtable</span></span>

### <span data-ttu-id="58209-155">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="58209-155">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="58209-156">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="58209-156">System.Int32</span></span>

### <span data-ttu-id="58209-157">AnalysisServices. PsAzureAnalysisServicesFirewallConfig/.</span><span class="sxs-lookup"><span data-stu-id="58209-157">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="58209-158">출력</span><span class="sxs-lookup"><span data-stu-id="58209-158">OUTPUTS</span></span>

### <span data-ttu-id="58209-159">AnalysisServices. AzureAnalysisServicesServer/.</span><span class="sxs-lookup"><span data-stu-id="58209-159">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="58209-160">상속자</span><span class="sxs-lookup"><span data-stu-id="58209-160">NOTES</span></span>
<span data-ttu-id="58209-161">별칭: Set-AzAs</span><span class="sxs-lookup"><span data-stu-id="58209-161">Alias: Set-AzAs</span></span>

## <span data-ttu-id="58209-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="58209-162">RELATED LINKS</span></span>

[<span data-ttu-id="58209-163">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="58209-163">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="58209-164">제거-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="58209-164">Remove-AzAnalysisServicesServer</span></span>](./Remove-AzAnalysisServicesServer.md)
