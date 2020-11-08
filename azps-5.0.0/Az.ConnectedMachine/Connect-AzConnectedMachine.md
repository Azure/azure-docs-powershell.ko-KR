---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/connect-azconnectedmachine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Connect-AzConnectedMachine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Connect-AzConnectedMachine.md
ms.openlocfilehash: 281d456eb7612914bac546b3d361238bb5056626
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216749"
---
# <span data-ttu-id="a7063-101">Connect-AzConnectedMachine</span><span class="sxs-lookup"><span data-stu-id="a7063-101">Connect-AzConnectedMachine</span></span>

## <span data-ttu-id="a7063-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7063-102">SYNOPSIS</span></span>
<span data-ttu-id="a7063-103">새 컴퓨터를 등록 하 여 ARM에서 추적 된 리소스를 만드는 API</span><span class="sxs-lookup"><span data-stu-id="a7063-103">API to register a new machine and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="a7063-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a7063-104">SYNTAX</span></span>

```
Connect-AzConnectedMachine [-ResourceGroupName] <String> [-Location] <String> [[-SubscriptionId] <String>]
 [[-Name] <String>] [[-DefaultProfile] <PSObject>] [[-PSSession] <PSSession[]>] [[-Tag] <Hashtable>]
 [[-Proxy] <Uri>] [<CommonParameters>]
```

## <span data-ttu-id="a7063-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a7063-105">DESCRIPTION</span></span>
<span data-ttu-id="a7063-106">새 컴퓨터를 등록 하 여 ARM에서 추적 된 리소스를 만드는 API</span><span class="sxs-lookup"><span data-stu-id="a7063-106">API to register a new machine and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="a7063-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a7063-107">EXAMPLES</span></span>

### <span data-ttu-id="a7063-108">예제 1: Onboards 연결 된 컴퓨터로 현재 컴퓨터</span><span class="sxs-lookup"><span data-stu-id="a7063-108">Example 1: Onboards the machine you're on as a connected machine</span></span>
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

<span data-ttu-id="a7063-109">Onboards 컴퓨터를 연결 된 컴퓨터로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a7063-109">Onboards the machine you're on as a connected machine.</span></span>

### <span data-ttu-id="a7063-110">예제 2: Onboards 원격 컴퓨터를 연결 된 장치로</span><span class="sxs-lookup"><span data-stu-id="a7063-110">Example 2: Onboards a remote machine as a connected device</span></span>
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

<span data-ttu-id="a7063-111">Onboards PowerShell remoting을 사용 하 여 원격 컴퓨터를 연결 된 장치로</span><span class="sxs-lookup"><span data-stu-id="a7063-111">Onboards a remote machine as a connected device using PowerShell remoting.</span></span>
<span data-ttu-id="a7063-112">참고:이 시점에는 대상 으로만 Windows가 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a7063-112">Note: only Windows as the target is supported at this time.</span></span>

## <span data-ttu-id="a7063-113">변수</span><span class="sxs-lookup"><span data-stu-id="a7063-113">PARAMETERS</span></span>

### <span data-ttu-id="a7063-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7063-114">-DefaultProfile</span></span>
<span data-ttu-id="a7063-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a7063-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7063-116">-위치</span><span class="sxs-lookup"><span data-stu-id="a7063-116">-Location</span></span>
<span data-ttu-id="a7063-117">생성 된 ConnectedMachine의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="a7063-117">The location for the created ConnectedMachine.</span></span>

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

### <span data-ttu-id="a7063-118">-이름</span><span class="sxs-lookup"><span data-stu-id="a7063-118">-Name</span></span>
<span data-ttu-id="a7063-119">이 컴퓨터에 사용 되는 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a7063-119">The name that will be used for this machine.</span></span>
<span data-ttu-id="a7063-120">호스트 이름이 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a7063-120">The hostname is used by default.</span></span>

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

### <span data-ttu-id="a7063-121">-프록시</span><span class="sxs-lookup"><span data-stu-id="a7063-121">-Proxy</span></span>
<span data-ttu-id="a7063-122">사용할 프록시 서버의 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="a7063-122">The URI for the proxy server to use</span></span>

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

### <span data-ttu-id="a7063-123">-PSSession</span><span class="sxs-lookup"><span data-stu-id="a7063-123">-PSSession</span></span>
<span data-ttu-id="a7063-124">이를 지정 하면 onboards에서 Azure로 작동 하는 명령이 각 PSSession 내에서 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a7063-124">When specified, the command that onboards machines to Azure will be run within each PSSession.</span></span>
<span data-ttu-id="a7063-125">참고:이는 현재 Windows 에서만 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7063-125">NOTE: This only works on Windows for now.</span></span>

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

### <span data-ttu-id="a7063-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7063-126">-ResourceGroupName</span></span>
<span data-ttu-id="a7063-127">컴퓨터를 추가 하려는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a7063-127">The name of the resource group you want to add the machine to.</span></span>

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

### <span data-ttu-id="a7063-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a7063-128">-SubscriptionId</span></span>
<span data-ttu-id="a7063-129">컴퓨터를 추가 하려는 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a7063-129">The ID of the subscription you want to add the machine to.</span></span>

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

### <span data-ttu-id="a7063-130">태그</span><span class="sxs-lookup"><span data-stu-id="a7063-130">-Tag</span></span>
<span data-ttu-id="a7063-131">리소스 태그.</span><span class="sxs-lookup"><span data-stu-id="a7063-131">Resource tags.</span></span>

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

### <span data-ttu-id="a7063-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7063-132">CommonParameters</span></span>
<span data-ttu-id="a7063-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7063-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7063-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a7063-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7063-135">입력</span><span class="sxs-lookup"><span data-stu-id="a7063-135">INPUTS</span></span>

## <span data-ttu-id="a7063-136">출력</span><span class="sxs-lookup"><span data-stu-id="a7063-136">OUTPUTS</span></span>

## <span data-ttu-id="a7063-137">상속자</span><span class="sxs-lookup"><span data-stu-id="a7063-137">NOTES</span></span>

<span data-ttu-id="a7063-138">별칭과</span><span class="sxs-lookup"><span data-stu-id="a7063-138">ALIASES</span></span>

## <span data-ttu-id="a7063-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a7063-139">RELATED LINKS</span></span>

