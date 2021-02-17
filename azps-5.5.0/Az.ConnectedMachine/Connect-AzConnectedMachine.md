---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/connect-azconnectedmachine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Connect-AzConnectedMachine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Connect-AzConnectedMachine.md
ms.openlocfilehash: 281d456eb7612914bac546b3d361238bb5056626
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209928"
---
# <span data-ttu-id="4454d-101">Connect-AzConnectedMachine</span><span class="sxs-lookup"><span data-stu-id="4454d-101">Connect-AzConnectedMachine</span></span>

## <span data-ttu-id="4454d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4454d-102">SYNOPSIS</span></span>
<span data-ttu-id="4454d-103">새 머신을 등록하여 새 머신에 추적된 리소스를 만드는 API를 ARM</span><span class="sxs-lookup"><span data-stu-id="4454d-103">API to register a new machine and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="4454d-104">구문</span><span class="sxs-lookup"><span data-stu-id="4454d-104">SYNTAX</span></span>

```
Connect-AzConnectedMachine [-ResourceGroupName] <String> [-Location] <String> [[-SubscriptionId] <String>]
 [[-Name] <String>] [[-DefaultProfile] <PSObject>] [[-PSSession] <PSSession[]>] [[-Tag] <Hashtable>]
 [[-Proxy] <Uri>] [<CommonParameters>]
```

## <span data-ttu-id="4454d-105">설명</span><span class="sxs-lookup"><span data-stu-id="4454d-105">DESCRIPTION</span></span>
<span data-ttu-id="4454d-106">새 머신을 등록하여 새 머신에 추적된 리소스를 만드는 API를 ARM</span><span class="sxs-lookup"><span data-stu-id="4454d-106">API to register a new machine and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="4454d-107">예제</span><span class="sxs-lookup"><span data-stu-id="4454d-107">EXAMPLES</span></span>

### <span data-ttu-id="4454d-108">예제 1: 연결된 컴퓨터로 사용 중 컴퓨터 온보드</span><span class="sxs-lookup"><span data-stu-id="4454d-108">Example 1: Onboards the machine you're on as a connected machine</span></span>
```powershell
PS C:\> Connect-AzConnectedMachine -ResourceGroupName contoso-connected-machines -Name linux_eastus1_1 -Location eastus

< truncated output of installing the azcmagent >

time="2020-08-07T13:13:25-07:00" level=info msg="Onboarding Machine. It usually takes a few minutes to complete. Sometimes it may take longer depending on network and server load status."
time="2020-08-07T13:13:25-07:00" level=info msg="Check network connectivity to all endpoints..."
time="2020-08-07T13:13:29-07:00" level=info msg="All endpoints are available... continue onboarding"
time="2020-08-07T13:13:50-07:00" level=info msg="Successfully Onboarded Resource to Azure" VM Id=978ab182-6cf0-4de3-a58b-53c8d0a3235e

Name             Location OSName   Status     ProvisioningState
----             -------- ------   ------     -----------------
linux_eastus1_1  eastus   linux    Connected  Succeeded
```

<span data-ttu-id="4454d-109">연결된 컴퓨터로 사용 중이신 머신을 온보드합니다.</span><span class="sxs-lookup"><span data-stu-id="4454d-109">Onboards the machine you're on as a connected machine.</span></span>

### <span data-ttu-id="4454d-110">예제 2: 원격 머신을 연결된 디바이스로 온보드</span><span class="sxs-lookup"><span data-stu-id="4454d-110">Example 2: Onboards a remote machine as a connected device</span></span>
```powershell
PS C:\> $session = Connect-PSSession -ComputerName WINBOX
PS C:\> Connect-AzConnectedMachine -ResourceGroupName contoso-rg -Name win_eastus1_1 -Location eastus -PSSession $session

< truncated output of installing the azcmagent >

time="2020-08-07T13:13:25-07:00" level=info msg="Onboarding Machine. It usually takes a few minutes to complete. Sometimes it may take longer depending on network and server load status."
time="2020-08-07T13:13:25-07:00" level=info msg="Check network connectivity to all endpoints..."
time="2020-08-07T13:13:29-07:00" level=info msg="All endpoints are available... continue onboarding"
time="2020-08-07T13:13:50-07:00" level=info msg="Successfully Onboarded Resource to Azure" VM Id=978ab182-6cf0-4de3-a58b-53c8d0a3236a

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
win_eastus1_1  eastus   windows  Connected  Succeeded
```

<span data-ttu-id="4454d-111">PowerShell 원격을 사용하여 원격 머신을 연결된 디바이스로 온보드합니다.</span><span class="sxs-lookup"><span data-stu-id="4454d-111">Onboards a remote machine as a connected device using PowerShell remoting.</span></span>
<span data-ttu-id="4454d-112">참고: 현재는 대상인 Windows만 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="4454d-112">Note: only Windows as the target is supported at this time.</span></span>

## <span data-ttu-id="4454d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4454d-113">PARAMETERS</span></span>

### <span data-ttu-id="4454d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4454d-114">-DefaultProfile</span></span>
<span data-ttu-id="4454d-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4454d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4454d-116">-Location</span><span class="sxs-lookup"><span data-stu-id="4454d-116">-Location</span></span>
<span data-ttu-id="4454d-117">생성된 ConnectedMachine의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="4454d-117">The location for the created ConnectedMachine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4454d-118">-Name</span><span class="sxs-lookup"><span data-stu-id="4454d-118">-Name</span></span>
<span data-ttu-id="4454d-119">이 머신에 사용할 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4454d-119">The name that will be used for this machine.</span></span>
<span data-ttu-id="4454d-120">호스트 이름은 기본적으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="4454d-120">The hostname is used by default.</span></span>

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

### <span data-ttu-id="4454d-121">-Proxy</span><span class="sxs-lookup"><span data-stu-id="4454d-121">-Proxy</span></span>
<span data-ttu-id="4454d-122">사용할 프록시 서버에 대한 URI</span><span class="sxs-lookup"><span data-stu-id="4454d-122">The URI for the proxy server to use</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4454d-123">-PSSession</span><span class="sxs-lookup"><span data-stu-id="4454d-123">-PSSession</span></span>
<span data-ttu-id="4454d-124">지정된 경우 Azure에 컴퓨터를 온보드하는 명령은 각 PSSession 내에서 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="4454d-124">When specified, the command that onboards machines to Azure will be run within each PSSession.</span></span>
<span data-ttu-id="4454d-125">참고: 지금은 Windows에서만 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="4454d-125">NOTE: This only works on Windows for now.</span></span>

```yaml
Type: System.Management.Automation.Runspaces.PSSession[]
Parameter Sets: (All)
Aliases: Session

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4454d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4454d-126">-ResourceGroupName</span></span>
<span data-ttu-id="4454d-127">머신을 추가할 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4454d-127">The name of the resource group you want to add the machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4454d-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4454d-128">-SubscriptionId</span></span>
<span data-ttu-id="4454d-129">머신을 추가하려는 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4454d-129">The ID of the subscription you want to add the machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4454d-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="4454d-130">-Tag</span></span>
<span data-ttu-id="4454d-131">리소스 태그.</span><span class="sxs-lookup"><span data-stu-id="4454d-131">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4454d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4454d-132">CommonParameters</span></span>
<span data-ttu-id="4454d-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4454d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4454d-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4454d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4454d-135">입력</span><span class="sxs-lookup"><span data-stu-id="4454d-135">INPUTS</span></span>

## <span data-ttu-id="4454d-136">출력</span><span class="sxs-lookup"><span data-stu-id="4454d-136">OUTPUTS</span></span>

## <span data-ttu-id="4454d-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4454d-137">NOTES</span></span>

<span data-ttu-id="4454d-138">별칭</span><span class="sxs-lookup"><span data-stu-id="4454d-138">ALIASES</span></span>

## <span data-ttu-id="4454d-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4454d-139">RELATED LINKS</span></span>

