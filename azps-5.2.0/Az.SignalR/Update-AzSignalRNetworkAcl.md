---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/update-azsignalrnetworkacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalRNetworkAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalRNetworkAcl.md
ms.openlocfilehash: afe9e1f604754c88035ed79f0eb480321ca348ba
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336081"
---
# <span data-ttu-id="feb85-101">Update-AzSignalRNetworkAcl</span><span class="sxs-lookup"><span data-stu-id="feb85-101">Update-AzSignalRNetworkAcl</span></span>

## <span data-ttu-id="feb85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="feb85-102">SYNOPSIS</span></span>
<span data-ttu-id="feb85-103">SignalR 서비스의 네트워크 ACL을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="feb85-103">Update the Network ACL of a SignalR service.</span></span>

## <span data-ttu-id="feb85-104">구문</span><span class="sxs-lookup"><span data-stu-id="feb85-104">SYNTAX</span></span>

### <span data-ttu-id="feb85-105">ResourceGroupParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="feb85-105">ResourceGroupParameterSet (Default)</span></span>
```
Update-AzSignalRNetworkAcl [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-DefaultAction <String>]
 [-PublicNetwork] [-PrivateEndpointName <String[]>] [-Allow <String[]>] [-Deny <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="feb85-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="feb85-106">ResourceIdParameterSet</span></span>
```
Update-AzSignalRNetworkAcl -ResourceId <String> [-AsJob] [-DefaultAction <String>] [-PublicNetwork]
 [-PrivateEndpointName <String[]>] [-Allow <String[]>] [-Deny <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="feb85-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="feb85-107">InputObjectParameterSet</span></span>
```
Update-AzSignalRNetworkAcl -InputObject <PSSignalRResource> [-AsJob] [-DefaultAction <String>] [-PublicNetwork]
 [-PrivateEndpointName <String[]>] [-Allow <String[]>] [-Deny <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="feb85-108">설명</span><span class="sxs-lookup"><span data-stu-id="feb85-108">DESCRIPTION</span></span>
<span data-ttu-id="feb85-109">기본 작업 및 공용 및 개인 연결에 대한 네트워크 Acl을 포함하여 SignalR 서비스의 네트워크 ACL을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="feb85-109">Update the Network ACL of a SignalR service, including the default action and the network Acls for public and private connection.</span></span>

## <span data-ttu-id="feb85-110">예제</span><span class="sxs-lookup"><span data-stu-id="feb85-110">EXAMPLES</span></span>

### <span data-ttu-id="feb85-111">공용 네트워크에 대한 RESTAPI, ClientConnection 허용 및 기본 작업을 거부로 설정</span><span class="sxs-lookup"><span data-stu-id="feb85-111">Allow RESTAPI,ClientConnection for public network and set default action to Deny</span></span>
```powershell
PS C:\> $networkAcl = Update-AzSignalRNetworkAcl -Name pssignalr -ResourceGroupName test_resource_group -DefaultAction Deny -PublicNetwork -Allow RESTAPI,ClientConnection

PS C:\>  $networkAcl

DefaultAction PublicNetwork                                        PrivateEndpoints
------------- -------------                                        ----------------
Deny          Microsoft.Azure.Commands.SignalR.Models.PSNetworkAcl {pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1}

PS C:\> $networkAcl.PublicNetwork
Allow                       Deny
-----                       ----
{ClientConnection, RESTAPI} {}
```

### <span data-ttu-id="feb85-112">개인 엔드포인트 연결에 클라이언트 연결 및 서버 연결 허용</span><span class="sxs-lookup"><span data-stu-id="feb85-112">Allow client connection and server connection for a private endpoint connection</span></span>
```powershell
PS C:\> $networkAcl = Update-AzSignalRNetworkAcl -Name pssignalr -ResourceGroupName test_resource_group -PrivateEndpointName pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1  -Allow ClientConnection,ServerConnection

PS C:\>$networkAcl.PrivateEndpoints[0]

Name                                           Allow                                Deny
----                                           -----                                ----
pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1 {ServerConnection, ClientConnection} {}
```

### <span data-ttu-id="feb85-113">공용 네트워크 및 개인 엔드포인트 연결 모두에 대한 클라이언트 연결 거부</span><span class="sxs-lookup"><span data-stu-id="feb85-113">Deny client connection for both public network and a private endpoint connection</span></span>
```powershell
PS C:\>$networkAcl = Update-AzSignalRNetworkAcl -Name pssignalr -ResourceGroupName test_resource_group -PrivateEndpointName pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1  -PublicNetwork -Deny ClientConnection
```

## <span data-ttu-id="feb85-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="feb85-114">PARAMETERS</span></span>

### <span data-ttu-id="feb85-115">-Allow</span><span class="sxs-lookup"><span data-stu-id="feb85-115">-Allow</span></span>
<span data-ttu-id="feb85-116">허용되는 네트워크 ACL</span><span class="sxs-lookup"><span data-stu-id="feb85-116">Allowed network ACLs</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: ClientConnection, ServerConnection, RESTAPI

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="feb85-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="feb85-117">-AsJob</span></span>
<span data-ttu-id="feb85-118">백그라운드 작업에서 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="feb85-118">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="feb85-119">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="feb85-119">-DefaultAction</span></span>
<span data-ttu-id="feb85-120">SignalR 네트워크 ACL의 기본 작업(허용 또는 거부)</span><span class="sxs-lookup"><span data-stu-id="feb85-120">Default Action of SignalR network ACLs, either allow or deny.</span></span> <span data-ttu-id="feb85-121">네트워크 ACL을 거부할지 아니면 네트워크 ACL이 적용될지 여부를 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="feb85-121">It decides whether deny network ACLs or allow network ACLs take effect.</span></span> <span data-ttu-id="feb85-122">예를 들어 기본 작업이 허용되는 경우 거부 ACL만 중요합니다.</span><span class="sxs-lookup"><span data-stu-id="feb85-122">For example, if the default action is allow, then only the deny ACLs matters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="feb85-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="feb85-123">-DefaultProfile</span></span>
<span data-ttu-id="feb85-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="feb85-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="feb85-125">-Deny</span><span class="sxs-lookup"><span data-stu-id="feb85-125">-Deny</span></span>
<span data-ttu-id="feb85-126">거부된 네트워크 ACL</span><span class="sxs-lookup"><span data-stu-id="feb85-126">Denied network ACLs</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: ClientConnection, ServerConnection, RESTAPI

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="feb85-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="feb85-127">-InputObject</span></span>
<span data-ttu-id="feb85-128">SignalR 리소스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="feb85-128">The SignalR resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="feb85-129">-Name</span><span class="sxs-lookup"><span data-stu-id="feb85-129">-Name</span></span>
<span data-ttu-id="feb85-130">SignalR 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="feb85-130">The SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="feb85-131">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="feb85-131">-PrivateEndpointName</span></span>
<span data-ttu-id="feb85-132">업데이트할 개인 엔드포인트의 이름</span><span class="sxs-lookup"><span data-stu-id="feb85-132">Name(s) of private endpoint(s) to be updated</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="feb85-133">-PublicNetwork</span><span class="sxs-lookup"><span data-stu-id="feb85-133">-PublicNetwork</span></span>
<span data-ttu-id="feb85-134">공용 네트워크 ACL 업데이트</span><span class="sxs-lookup"><span data-stu-id="feb85-134">Update public network ACLs</span></span>

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

### <span data-ttu-id="feb85-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="feb85-135">-ResourceGroupName</span></span>
<span data-ttu-id="feb85-136">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="feb85-136">The resource group name.</span></span>
<span data-ttu-id="feb85-137">지정하지 않으면 기본 기본 설정이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="feb85-137">The default one will be used if not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="feb85-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="feb85-138">-ResourceId</span></span>
<span data-ttu-id="feb85-139">SignalR Service 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="feb85-139">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="feb85-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="feb85-140">-Confirm</span></span>
<span data-ttu-id="feb85-141">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="feb85-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="feb85-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="feb85-142">-WhatIf</span></span>
<span data-ttu-id="feb85-143">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="feb85-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="feb85-144">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="feb85-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="feb85-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="feb85-145">CommonParameters</span></span>
<span data-ttu-id="feb85-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="feb85-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="feb85-147">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="feb85-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="feb85-148">입력</span><span class="sxs-lookup"><span data-stu-id="feb85-148">INPUTS</span></span>

### <span data-ttu-id="feb85-149">System.String</span><span class="sxs-lookup"><span data-stu-id="feb85-149">System.String</span></span>

## <span data-ttu-id="feb85-150">출력</span><span class="sxs-lookup"><span data-stu-id="feb85-150">OUTPUTS</span></span>

### <span data-ttu-id="feb85-151">Microsoft.Azure.Commands.SignalR.Models.PSSignalRNetworkAcls</span><span class="sxs-lookup"><span data-stu-id="feb85-151">Microsoft.Azure.Commands.SignalR.Models.PSSignalRNetworkAcls</span></span>

## <span data-ttu-id="feb85-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="feb85-152">NOTES</span></span>

## <span data-ttu-id="feb85-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="feb85-153">RELATED LINKS</span></span>
