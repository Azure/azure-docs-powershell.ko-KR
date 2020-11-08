---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/update-azsignalrnetworkacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalRNetworkAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalRNetworkAcl.md
ms.openlocfilehash: afe9e1f604754c88035ed79f0eb480321ca348ba
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226658"
---
# <span data-ttu-id="47704-101">Update-AzSignalRNetworkAcl</span><span class="sxs-lookup"><span data-stu-id="47704-101">Update-AzSignalRNetworkAcl</span></span>

## <span data-ttu-id="47704-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47704-102">SYNOPSIS</span></span>
<span data-ttu-id="47704-103">SignalR 서비스의 네트워크 ACL을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="47704-103">Update the Network ACL of a SignalR service.</span></span>

## <span data-ttu-id="47704-104">구문과</span><span class="sxs-lookup"><span data-stu-id="47704-104">SYNTAX</span></span>

### <span data-ttu-id="47704-105">ResourceGroupParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="47704-105">ResourceGroupParameterSet (Default)</span></span>
```
Update-AzSignalRNetworkAcl [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-DefaultAction <String>]
 [-PublicNetwork] [-PrivateEndpointName <String[]>] [-Allow <String[]>] [-Deny <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47704-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="47704-106">ResourceIdParameterSet</span></span>
```
Update-AzSignalRNetworkAcl -ResourceId <String> [-AsJob] [-DefaultAction <String>] [-PublicNetwork]
 [-PrivateEndpointName <String[]>] [-Allow <String[]>] [-Deny <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47704-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="47704-107">InputObjectParameterSet</span></span>
```
Update-AzSignalRNetworkAcl -InputObject <PSSignalRResource> [-AsJob] [-DefaultAction <String>] [-PublicNetwork]
 [-PrivateEndpointName <String[]>] [-Allow <String[]>] [-Deny <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47704-108">설명은</span><span class="sxs-lookup"><span data-stu-id="47704-108">DESCRIPTION</span></span>
<span data-ttu-id="47704-109">기본 동작과 공용 및 개인 연결에 대 한 네트워크 Acl을 포함 하 여 SignalR 서비스의 네트워크 ACL을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="47704-109">Update the Network ACL of a SignalR service, including the default action and the network Acls for public and private connection.</span></span>

## <span data-ttu-id="47704-110">예제의</span><span class="sxs-lookup"><span data-stu-id="47704-110">EXAMPLES</span></span>

### <span data-ttu-id="47704-111">공용 네트워크에 대해 RESTAPI, ClientConnection을 허용 하 고 기본 작업을 거부로 설정</span><span class="sxs-lookup"><span data-stu-id="47704-111">Allow RESTAPI,ClientConnection for public network and set default action to Deny</span></span>
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

### <span data-ttu-id="47704-112">개인 끝점 연결에 대 한 클라이언트 연결 및 서버 연결 허용</span><span class="sxs-lookup"><span data-stu-id="47704-112">Allow client connection and server connection for a private endpoint connection</span></span>
```powershell
PS C:\> $networkAcl = Update-AzSignalRNetworkAcl -Name pssignalr -ResourceGroupName test_resource_group -PrivateEndpointName pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1  -Allow ClientConnection,ServerConnection

PS C:\>$networkAcl.PrivateEndpoints[0]

Name                                           Allow                                Deny
----                                           -----                                ----
pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1 {ServerConnection, ClientConnection} {}
```

### <span data-ttu-id="47704-113">공용 네트워크와 개인 끝점 연결 모두에 대 한 클라이언트 연결 거부</span><span class="sxs-lookup"><span data-stu-id="47704-113">Deny client connection for both public network and a private endpoint connection</span></span>
```powershell
PS C:\>$networkAcl = Update-AzSignalRNetworkAcl -Name pssignalr -ResourceGroupName test_resource_group -PrivateEndpointName pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1  -PublicNetwork -Deny ClientConnection
```

## <span data-ttu-id="47704-114">변수</span><span class="sxs-lookup"><span data-stu-id="47704-114">PARAMETERS</span></span>

### <span data-ttu-id="47704-115">-허용</span><span class="sxs-lookup"><span data-stu-id="47704-115">-Allow</span></span>
<span data-ttu-id="47704-116">허용 된 네트워크 Acl</span><span class="sxs-lookup"><span data-stu-id="47704-116">Allowed network ACLs</span></span>

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

### <span data-ttu-id="47704-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="47704-117">-AsJob</span></span>
<span data-ttu-id="47704-118">백그라운드 작업에서 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="47704-118">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="47704-119">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="47704-119">-DefaultAction</span></span>
<span data-ttu-id="47704-120">SignalR 네트워크 Acl의 기본 작업으로 허용 또는 거부입니다.</span><span class="sxs-lookup"><span data-stu-id="47704-120">Default Action of SignalR network ACLs, either allow or deny.</span></span> <span data-ttu-id="47704-121">이는 네트워크 Acl 거부 또는 네트워크 Acl 허용이 적용 되는지 여부를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="47704-121">It decides whether deny network ACLs or allow network ACLs take effect.</span></span> <span data-ttu-id="47704-122">예를 들어 기본 작업을 허용 하는 경우 Acl 거부만 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="47704-122">For example, if the default action is allow, then only the deny ACLs matters.</span></span>

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

### <span data-ttu-id="47704-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47704-123">-DefaultProfile</span></span>
<span data-ttu-id="47704-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="47704-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47704-125">-Deny</span><span class="sxs-lookup"><span data-stu-id="47704-125">-Deny</span></span>
<span data-ttu-id="47704-126">네트워크 Acl 거부</span><span class="sxs-lookup"><span data-stu-id="47704-126">Denied network ACLs</span></span>

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

### <span data-ttu-id="47704-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="47704-127">-InputObject</span></span>
<span data-ttu-id="47704-128">SignalR resource 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="47704-128">The SignalR resource object.</span></span>

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

### <span data-ttu-id="47704-129">-이름</span><span class="sxs-lookup"><span data-stu-id="47704-129">-Name</span></span>
<span data-ttu-id="47704-130">SignalR 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="47704-130">The SignalR service name.</span></span>

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

### <span data-ttu-id="47704-131">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="47704-131">-PrivateEndpointName</span></span>
<span data-ttu-id="47704-132">업데이트 될 개인 끝점의 이름 (들)</span><span class="sxs-lookup"><span data-stu-id="47704-132">Name(s) of private endpoint(s) to be updated</span></span>

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

### <span data-ttu-id="47704-133">-PublicNetwork</span><span class="sxs-lookup"><span data-stu-id="47704-133">-PublicNetwork</span></span>
<span data-ttu-id="47704-134">공용 네트워크 Acl 업데이트</span><span class="sxs-lookup"><span data-stu-id="47704-134">Update public network ACLs</span></span>

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

### <span data-ttu-id="47704-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47704-135">-ResourceGroupName</span></span>
<span data-ttu-id="47704-136">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="47704-136">The resource group name.</span></span>
<span data-ttu-id="47704-137">지정 되지 않은 경우 기본 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="47704-137">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="47704-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="47704-138">-ResourceId</span></span>
<span data-ttu-id="47704-139">SignalR 서비스 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="47704-139">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="47704-140">-확인</span><span class="sxs-lookup"><span data-stu-id="47704-140">-Confirm</span></span>
<span data-ttu-id="47704-141">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="47704-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47704-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47704-142">-WhatIf</span></span>
<span data-ttu-id="47704-143">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="47704-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47704-144">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="47704-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47704-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47704-145">CommonParameters</span></span>
<span data-ttu-id="47704-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="47704-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47704-147">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="47704-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47704-148">입력</span><span class="sxs-lookup"><span data-stu-id="47704-148">INPUTS</span></span>

### <span data-ttu-id="47704-149">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="47704-149">System.String</span></span>

## <span data-ttu-id="47704-150">출력</span><span class="sxs-lookup"><span data-stu-id="47704-150">OUTPUTS</span></span>

### <span data-ttu-id="47704-151">SignalR. PSSignalRNetworkAcls/.</span><span class="sxs-lookup"><span data-stu-id="47704-151">Microsoft.Azure.Commands.SignalR.Models.PSSignalRNetworkAcls</span></span>

## <span data-ttu-id="47704-152">상속자</span><span class="sxs-lookup"><span data-stu-id="47704-152">NOTES</span></span>

## <span data-ttu-id="47704-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="47704-153">RELATED LINKS</span></span>
